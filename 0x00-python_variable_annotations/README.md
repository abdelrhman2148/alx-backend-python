# 0x00. Python - Variable Annotations

## Description
This project covers advanced Python concepts, specifically focusing on variable annotations introduced in Python 3. It helps you understand how to use type annotations to enhance code readability, improve function signatures, and ensure better type safety during development.

## Learning Objectives
By the end of this project, you will:
- Understand type annotations in Python 3.
- Know how to specify function signatures and variable types using annotations.
- Be familiar with duck typing.
- Learn to validate your code with mypy.

## Requirements
- Python version: `python3 (3.7)`
- All code should be compatible with `Ubuntu 18.04 LTS`.
- Code should adhere to `pycodestyle` (version 2.5).
- All files must end with a new line and be executable.
- Each file should begin with `#!/usr/bin/env python3`.

## Concepts Covered
1. **Type Annotations**:
   - Specifying data types for function arguments and return values.
   - Variables and function signatures must use proper typing.
2. **Duck Typing**:
   - Using type hints in a way that is flexible and aligns with Python’s dynamic nature.
3. **Type Validation**:
   - Using `mypy` to check type correctness and ensure code accuracy.
4. **Complex Types**:
   - Working with `List`, `Tuple`, `Union`, and `Callable` types.

## Tasks
1. **Basic annotations - add**:
   Write a type-annotated function `add` that takes two floats and returns their sum.

2. **Basic annotations - concat**:
   Write a type-annotated function `concat` that concatenates two strings.

3. **Basic annotations - floor**:
   Write a function `floor` that returns the floor of a float.

4. **Basic annotations - to string**:
   Write a function `to_str` that converts a float to its string representation.

5. **Define variables**:
   Define and annotate variables with specific types and values (int, float, bool, string).

6. **Complex types - list of floats**:
   Write a function `sum_list` that takes a list of floats and returns their sum.

7. **Complex types - mixed list**:
   Write a function `sum_mixed_list` that handles a list of integers and floats and returns their sum.

8. **Complex types - string and int/float to tuple**:
   Write a function `to_kv` that returns a tuple where the second element is the square of an int/float.

9. **Complex types - functions**:
   Write a function `make_multiplier` that returns another function that multiplies a float by a given multiplier.

10. **Duck typing - first element of a sequence**:
   Use duck typing to annotate a function that returns the first element of a sequence.

## Advanced Tasks
1. **More involved type annotations**:
   Add complex type annotations to functions with varied return types using `TypeVar`.

2. **Type checking**:
   Use `mypy` to validate the type correctness of a Python function involving tuples and lists.

## Repo Structure
```bash
.
├── 0-add.py
├── 1-concat.py
├── 2-floor.py
├── 3-to_str.py
├── 4-define_variables.py
├── 5-sum_list.py
├── 6-sum_mixed_list.py
├── 7-to_kv.py
├── 8-make_multiplier.py
├── 9-element_length.py
├── 100-safe_first_element.py
├── 101-safely_get_value.py
├── 102-type_checking.py
└── README.md
```

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/alx-backend-python.git
   ```
2. Navigate to the project directory:
   ```bash
   cd 0x00-python_variable_annotations
   ```
3. Run the Python files:
   ```bash
   ./0-add.py
   ./1-concat.py
   ```

## Validation
To validate your type annotations, use `mypy`:
```bash
mypy file_name.py
```
