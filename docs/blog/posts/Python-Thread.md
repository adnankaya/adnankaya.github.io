---
date:
  created: 2024-09-22
  updated: 2024-09-23
readtime: 4
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
  - thread
  - parallel
authors:
  - adnankaya
slug: understanding-python-thread
---

# Understanding Python Threads

Let's understand python's threads!

<!-- more -->

Imagine you’re running a bakery, and it’s the busiest time of the year. Customers are pouring in for cakes, pastries, and freshly baked bread. Now, if you only had one baker handling everything, it would take forever to fulfill all the orders. That baker would have to mix the dough, bake the bread, decorate the cakes, and handle the cash register—all one task at a time. This is inefficient and slow.

Now, let's bring in threads to save the day. Threads are like hiring multiple bakers, each with a specific job. While one baker decorates the cakes, another is mixing the dough, and yet another is handling the cash register. This way, multiple tasks are happening at the same time, and the bakery runs smoothly without any bottlenecks. Each baker (or thread) works independently on their own task, but they all contribute to the overall work being done.

## Built-in Threads: Doing Multiple Things at Once

In Python, threads are like these bakers—mini-workers that allow your program to do several things at once without waiting for one task to finish before starting the next.

Let’s say you’re managing a small program that needs to bake cakes and serve coffee simultaneously. If you handle these tasks one by one, you might keep customers waiting too long for their coffee while cakes are baking. So, you use threads to parallelize these tasks.

Here’s how threading can help:
```python
import threading

def bake_cake():
    print("Cake is baking...")

def serve_coffee():
    print("Serving coffee...")

# Creating threads
cake_thread = threading.Thread(target=bake_cake)
coffee_thread = threading.Thread(target=serve_coffee)

# Starting the threads
cake_thread.start()
coffee_thread.start()

# Ensuring both tasks are completed before moving on
cake_thread.join()
coffee_thread.join()

```

In this example, the bakery now has one baker handling cake-baking while another serves coffee. Both tasks run at the same time, ensuring customers are happy and your bakery stays efficient.

## When to Write Custom Threads

Now, think about your bakery growing even more. You have multiple customers placing custom orders at the same time. One person wants a birthday cake, another wants cupcakes, and yet another wants a wedding cake. You could assign each of these orders to a specific baker. But what if one baker finishes early or gets stuck on a complex decoration? You want a system where bakers can hand off tasks and ensure none of them stand idle.

This is where you may write your own custom thread management system. You want to ensure that if one thread finishes early or gets blocked (maybe a cake takes longer to bake), the other threads continue working without waiting.

## Custom Thread Management

In Python, writing a custom thread manager could look something like this:
```python
import threading

class BakeryThread(threading.Thread):
    def __init__(self, task, name):
        threading.Thread.__init__(self)
        self.task = task
        self.name = name
    
    def run(self):
        print(f"{self.name} is starting to work on {self.task}")
        # Simulate work with a delay
        import time
        time.sleep(2)
        print(f"{self.name} has finished {self.task}")

# Create custom threads for each order
thread1 = BakeryThread("baking birthday cake", "Baker 1")
thread2 = BakeryThread("decorating cupcakes", "Baker 2")
thread3 = BakeryThread("baking wedding cake", "Baker 3")

# Start the threads
thread1.start()
thread2.start()
thread3.start()

# Wait for all threads to complete
thread1.join()
thread2.join()
thread3.join()

```

In this scenario, each baker (or thread) is assigned a specific task. They work independently but complete their tasks in parallel. By creating custom threads, you gain control over how each "baker" (thread) works and how they interact.

## Why Write Custom Threads?

You'd need custom threads when you have complex workflows that involve multiple steps or when some tasks need to interact carefully with others. In the real world, custom threads are used for:

- Handling multiple user requests in a web application simultaneously.
- Downloading files from the internet while performing other tasks.
- Running background tasks like data processing or periodic checks without slowing down the main application.

## Avoiding Pitfalls
However, just like too many bakers crowding the kitchen, using too many threads can lead to problems. If threads aren’t coordinated well, they can step on each other’s toes (like trying to access the same oven or file), leading to bugs and issues. That’s where locks and thread synchronization come in, ensuring the bakers wait their turn when necessary, like sharing the same oven.

## Conclusion
In summary, threads allow your "bakery" (program) to handle multiple tasks at once, boosting efficiency and ensuring things get done quickly. Whether you’re handling simple tasks like serving coffee or more complex ones like custom orders, threads make sure everything runs in parallel—just like bakers in a busy kitchen!
