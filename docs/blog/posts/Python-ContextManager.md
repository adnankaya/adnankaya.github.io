---
date:
  created: 2024-09-22
  updated: 2024-09-23
readtime: 3
pin: true
links:
  - Homepage: index.md#project-layout
  - Blog index: blog/index.md
  - External links:
    - Web Page: https://adnankaya.github.io
categories:
  - Python
tags:
  - python
  - context manager
  - article
authors:
  - adnankaya
slug: understanding-python-context-manager
---

# Understanding Python Context Managers

Let's understand python's context managers!

<!-- more -->

Imagine you're managing a high-end restaurant, where every evening, guests arrive to enjoy a fine dining experience. In this scenario, you want everything to run smoothly — from preparing the tables to ensuring guests leave happy. But there’s a catch: You need to make sure the restaurant is perfectly cleaned and set up before opening, and thoroughly cleaned again after closing. This entire process needs to happen daily, or chaos will ensue!

Now, think of context managers in Python as a system that ensures this sequence runs perfectly every time. The restaurant is your program, and the setup and cleanup are the tasks that must happen before and after certain operations.

## The Built-in Context Manager: Opening a File

Let’s first look at a simple, everyday scenario in Python: opening and reading a file. Without context managers, managing this could feel like opening the restaurant but forgetting to clean up afterward. You could have issues like leaving the file open and consuming system resources (just like not cleaning tables after the guests leave!).

Here’s how context managers make sure everything is cleaned up:
```python
with open('menu.txt', 'r') as file:
    contents = file.read()
```

In this case, Python is the responsible restaurant manager. The file (our restaurant) is opened, the contents are read (our guests are served), and afterward, the file is closed automatically (the cleanup). We don’t have to manually close the file, as Python does it for us.

## The Need for a Custom Context Manager

But now imagine you’re managing a more complex scenario: a special section of the restaurant with expensive teas. Before the guests can enter this section, the staff needs to check the tea temperature, adjust lighting, and set up exclusive decorations. And after the guests leave, all of this needs to be reverted carefully. You want this to happen automatically every time someone books the section.

In Python terms, this is where you’d write your own custom context manager. You need to ensure that before certain operations start, a setup occurs (setting the mood), and after the operation ends, a cleanup happens (reverting the decorations).

### Writing a Custom Context Manager

Here’s an example of a custom context manager to mimic this restaurant scenario:

```python
class TeaSectionManager:
    def __enter__(self):
        print("Preparing the exclusive tea section...")  # Setup tasks
        # Code to set the right tea temperature, adjust lighting, etc.
        return self
    
    def __exit__(self, exc_type, exc_value, traceback):
        print("Reverting tea section setup...")  # Cleanup tasks
        # Code to clean and reset the section back to normal

# Using the context manager
with TeaSectionManager():
    print("Guests are enjoying the exclusive tea section.")

```

### Why Write Custom Context Managers?

We write custom context managers when we have resources that need precise setup and cleanup. Examples in real-world programming include:

- **Database connections**: Opening a database connection before querying and closing it afterward.
- **Locks**: In multithreading, acquiring a lock before a critical section and releasing it afterward.
- **Network connections**: Managing socket connections that need to be opened and closed properly.

Just like the tea section in the restaurant, custom context managers handle more complex processes that involve multiple steps and ensure that no matter what happens (even if an error occurs), the cleanup is always done correctly. It keeps your program organized and prevents resource leaks or issues.

### Conclusion
In short, context managers ensure smooth operation before and after certain tasks, whether it's as simple as opening a file or as complex as managing exclusive services in a restaurant. And when Python’s built-in context managers don’t cover a situation, writing your own lets you take control and ensure everything runs seamlessly!
