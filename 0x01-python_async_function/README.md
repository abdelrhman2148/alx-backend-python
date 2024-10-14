# 0x01. Python - Async

This repository contains Python scripts that demonstrate asynchronous programming concepts using asyncio and async/await syntax.

## Resources

Read or watch:
- [Async IO in Python: A Complete Walkthrough](https://realpython.com/async-io-python/)
- [asyncio - Asynchronous I/O](https://docs.python.org/3/library/asyncio.html)
- [random.uniform](https://docs.python.org/3/library/random.html#random.uniform)

## Learning Objectives

By the end of this project, you should be able to explain to anyone:
- async and await syntax in Python
- How to execute an async program with asyncio
- How to run concurrent coroutines
- How to create asyncio tasks
- How to use the random module in async functions

## Requirements

### General
- A README.md file, at the root of the folder of the project, is mandatory
- Allowed editors: vi, vim, emacs
- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7)
- All your files should end with a new line
- All your files must be executable
- The length of your files will be tested using wc
- The first line of all your files should be exactly `#!/usr/bin/env python3`
- Your code should use the pycodestyle style (version 2.5.x)
- All your functions and coroutines must be type-annotated.
- All your modules should have a documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
- All your functions should have a documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`)
- A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)

## Tasks

### 0. The basics of async
Write an asynchronous coroutine `wait_random` that takes in an integer argument `max_delay` (default value 10) and returns a float delayed by a random number of seconds between 0 and `max_delay`.

### 1. Let's execute multiple coroutines at the same time with async
Write an async function `wait_n` that takes in two integers `n` and `max_delay`. It spawns `wait_random` `n` times with the specified `max_delay` and returns a sorted list of delays.

### 2. Measure the runtime
Write a function `measure_time` that measures the total execution time for `wait_n(n, max_delay)` and returns the average time per coroutine execution.

### 3. Tasks
Write a function `task_wait_random` that returns an asyncio.Task for `wait_random`.

### 4. Tasks
Modify `wait_n` into `task_wait_n` that uses `task_wait_random` to spawn tasks instead of calling `wait_random`.

## Repository Structure

- GitHub repository: [alx-backend-python](https://github.com/your-username/alx-backend-python)
- Directory: 0x01-python_async_function
- Files:
  - `0-basic_async_syntax.py`
  - `1-concurrent_coroutines.py`
  - `2-measure_runtime.py`
  - `3-tasks.py`
  - `4-tasks.py`
