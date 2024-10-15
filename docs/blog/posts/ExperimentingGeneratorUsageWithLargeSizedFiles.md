---
date:
  created: 2024-10-15
  updated: 2024-10-16
readtime: 10
pin: false
links:
  - Homepage: index.md#project-layout
  - Blog index: blog/index.md
  - External links:
    - Web Page: https://adnankaya.github.io
categories:
  - Python
tags:
  - python
  - generator
  - optimization
authors:
  - adnankaya
slug: experimenting-generator-usage-with-large-sized-files-in-python
---

# Experimenting Generator Usage with Large Sized Files in Python

We always read that generators are memory friendly. It is not recommended to load a large sized file into memory because it can cause memory leak problem. I wanted to experiment this issue.

<!-- more -->


## What we are going to learn?
1. How memory gets affected when we load a large sized file (Mine is 837 MB) ?
2. What happens when we have limited memory if large file is loaded?
3. How can we use generators to write memory friendly code?

## What we need to experiment ?
1. Docker
2. Large sized txt file (I do have a simple script to generate if you dont have.)

- Let's create a directory `mkdir pylab`
- Let's continue by creating a super simple `Dockerfile` for python.

```Dockerfile
FROM python:3.12.4-slim

WORKDIR /app

COPY . .

```
### Files & Folders

- Let's see what we have in `pylab`
```bash

├── Dockerfile
├── largefile.txt # my large sized file
└── run_generate_largefile.py # python file to generate large file

0 directories, 3 files

```

> Without Docker you can to this experiment but I will be limiting our container to blow up memory as well.

## Experimenting Starts

### 1. Build Docker Image and Run The Container

- Run following command to build the image (in the `pylab` directory)
```bash
# cd pylab
docker build -t py-playground .
```
- `py-playground` is our image name
- `.` means current directory!


- We built the image and now its time to run the image (`py-playground`)
```bash
docker run --rm --name experiment-generators -it --entrypoint bash py-playground
```
- `--rm` : removes the stopped container when we also exit from the container.
- `--name OUR-CONTAINER-NAME`: to give a name for our container
- `--entrypoint bash` : to run bash in the container 
- more -> `docker run --help`

Above command should navigate you following (your container id may be different)
```bash
root@319cc9645884:/app# 
```
- Let's see what we have in our container
```bash
root@319cc9645884:/app# ls -alhS
total 837M
-rw-r--r-- 1 root root 837M Oct  1 05:54 largefile.txt
drwxr-xr-x 1 root root 4.0K Oct  1 08:47 .
drwxr-xr-x 1 root root 4.0K Oct  1 08:59 ..
-rw-r--r-- 1 root root  377 Oct  1 07:43 run_generate_largefile.py
-rw-r--r-- 1 root root  138 Oct  1 06:04 .dockerignore
-rw-r--r-- 1 root root   48 Oct  1 07:49 Dockerfile

```

### 2. Display Container Stats
- **Open a new terminal**
- Before running python shell let's run the `docker stats` command in the new terminal
```bash
docker stats
```

- Output
```bash
CONTAINER ID   NAME                    CPU %     MEM USAGE / LIMIT   MEM %     NET I/O       BLOCK I/O   PIDS
319cc9645884   experiment-generators   0.00%     852KiB / 7.668GiB   0.01%     1.09kB / 0B   0B / 0B     1
```

- **Go back to docker container terminal** and run the python shell
```bash
root@319cc9645884:/app# python
Python 3.12.4 (main, Aug  1 2024, 21:12:58) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```
- Let's see `dockert stats` again in other terminal
```bash
CONTAINER ID   NAME                    CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O       PIDS
319cc9645884   experiment-generators   0.00%     11.92MiB / 7.668GiB   0.15%     1.16kB / 0B   778kB / 872kB   2
```

## Memory Usage 1

|Before|After    |
|------|---------|
|852 KiB|11.92 MiB|

- Go back to python terminal and open the file and readlines

```bash
# in the python container

Python 3.12.4 (main, Aug  1 2024, 21:12:58) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> o = open("largefile.txt", "r")# 1. open the file in reading mode
>>> content = o.readlines() # read all lines and assign to content variable, loaded into memory!

```

- Check the `docker stats` again in other terminal

```bash
CONTAINER ID   NAME                    CPU %     MEM USAGE / LIMIT     MEM %     NET I/O       BLOCK I/O        PIDS
319cc9645884   experiment-generators   0.00%     6.796GiB / 7.668GiB   88.63%    1.23kB / 0B   243MB / 17.3MB   2

```
> **Remember largefile.txt is 837 MB**
    
## Memory Usage 2

|Before|After    |
|------|---------|
|852 KiB|11.92 MiB|
|11.92 MiB|6.769 **GiB**|

- **As we can see that loading all the file content into memory is inefficient**

- Let's free our memory by deleting the reference `content` and then python garbage collector will do its job.
```bash
# >>> o = open("largefile.txt", "r")
# >>> content = o.readlines()
>>> del content
```

## Memory Usage 3

|Before|After    |
|------|---------|
|852 KiB|11.92 MiB|
|11.92 MiB|6.769 **GiB**|
|6.769 **GiB**|62.93 MiB|

### What are the efficient ways to read file?

We can [loop over](https://docs.python.org/3/tutorial/inputoutput.html#methods-of-file-objects) the file object to read file content fast and efficiently.

```bash
>>> def read_10_lines(fileobject):
...     counter = 0
...     for line in fileobject:
...         print(line, end='')
...         counter +=1
...         if counter > 10:
...             break
>>>
>>> o = open("largefile.txt", "r")
>>> read_10_lines(o)
0.0.0.0
1.1.1.1
2.2.2.2
3.3.3.3
4.4.4.4
5.5.5.5
6.6.6.6
7.7.7.7
8.8.8.8
9.9.9.9
10.10.10.10
>>> o.close()

```

## Memory Usage 4

|Memory Stats |Before|After           |
|-------------|------|----------------|
|docker stats |852 KiB|11.92 MiB      |
|docker stats |11.92 MiB|6.769 **GiB**|
|docker stats |6.769 **GiB**|62.93 MiB|
|docker stats |62.93 MiB|64.6 MiB     |

- Example generator usage

```python

def process_data(lines):
    """process the lines data"""
    pass

def filegenerator(fileobj, chunk=1024):
    """
    params
    fileobj -- instance of file object
    chunk -- how many items will be processed
    """
    while True:
        lines = fileobj.readlines(chunk)
        if not lines:
            break
        yield lines

with open("largefile.txt", "r") as fileobj:
    lines = filegenerator(fileobj, chunk=2**16) # 2^16 is 65536 
    process_data(lines)

```


