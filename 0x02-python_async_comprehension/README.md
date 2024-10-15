# 0x02. Python - Async Comprehension

This project focuses on asynchronous programming in Python, specifically working with **async generators** and **async comprehensions**. You will learn how to write asynchronous code, perform asynchronous operations, and handle asynchronous data using Python's `async` and `await` syntax.

## Learning Objectives

By the end of this project, you should be able to:
- Write an **asynchronous generator**.
- Use **async comprehensions** to work with asynchronous data.
- **Type-annotate** generators and asynchronous functions.
- Measure runtime for asynchronous tasks running in parallel.

## Resources

- [PEP 530 – Asynchronous Comprehensions](https://www.python.org/dev/peps/pep-0530/)
- [What’s New in Python: Asynchronous Comprehensions / Generators](https://docs.python.org/3/whatsnew/3.6.html#whatsnew36-pep530)
- [Type-hints for Generators](https://mypy.readthedocs.io/en/stable/generics.html#async-generators)

## Requirements

- All your files will be interpreted/compiled on **Ubuntu 18.04 LTS** using `python3` (version 3.7).
- All files should end with a new line.
- The first line of all your files should be exactly `#!/usr/bin/env python3`.
- Your code should follow the **pycodestyle** style guide (version 2.5.x).
- Each module and function must be documented with a docstring.
- All functions and coroutines must be **type-annotated**.
- A `README.md` file is mandatory at the root of the project directory.

## Project Structure

- GitHub repository: **[alx-backend-python](https://github.com/your-username/alx-backend-python)**
- Directory: `0x02-python_async_comprehension`

## Tasks

### Task 0: Async Generator

Write a coroutine called `async_generator` that:
- Loops 10 times.
- Asynchronously waits for 1 second each time.
- Yields a random float number between 0 and 10.

#### Example:
```python
import asyncio
from random import uniform

async def async_generator():
    for _ in range(10):
        await asyncio.sleep(1)
        yield uniform(0, 10)
```

**File**: `0-async_generator.py`

### Task 1: Async Comprehension

Write a coroutine called `async_comprehension` that:
- Collects 10 random numbers using an async comprehension over `async_generator`.
- Returns the list of 10 numbers.

#### Example:
```python
import asyncio
from .async_generator import async_generator

async def async_comprehension():
    return [i async for i in async_generator()]
```

**File**: `1-async_comprehension.py`

### Task 2: Run Time for Four Parallel Comprehensions

Write a coroutine called `measure_runtime` that:
- Executes `async_comprehension` four times in parallel using `asyncio.gather`.
- Measures and returns the total runtime.

#### Example:
```python
import asyncio
from .async_comprehension import async_comprehension

async def measure_runtime():
    start_time = asyncio.get_event_loop().time()
    await asyncio.gather(*(async_comprehension() for _ in range(4)))
    return asyncio.get_event_loop().time() - start_time
```

**File**: `2-measure_runtime.py`

### Example Output:
```bash
$ ./2-main.py
10.021936893463135
```

The total runtime is approximately **10 seconds** because each `async_comprehension` takes 10 seconds to complete, and all four run in parallel.

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/alx-backend-python.git
   cd alx-backend-python/0x02-python_async_comprehension
   ```

2. Run each task:
   ```bash
   python3 0-main.py
   python3 1-main.py
   python3 2-main.py
   ```

## Additional Resources
- [Asyncio in Python: A Complete Walkthrough](https://realpython.com/async-io-python/)
- [Understanding Python's async and await](https://medium.com/python-in-plain-english/understanding-pythons-async-await-87b9928a9f44)


Happy Coding!

This `README.md` provides a comprehensive overview of the project, covering learning objectives, tasks, example code, file structure, and how to run the project.
