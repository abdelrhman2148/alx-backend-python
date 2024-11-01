# 0x03. Unittests and Integration Tests

This project involves creating and running both unit and integration tests for various backend Python functions and classes. You'll learn to mock dependencies, parameterize tests, and organize tests using fixtures, aiming to validate both individual components and end-to-end functionality of the codebase.

## Learning Objectives

By the end of this project, you should be able to:
- Differentiate between unit and integration tests.
- Use common testing patterns such as mocking, parameterization, and fixtures.
- Execute tests using the `unittest` framework in Python.

## Project Requirements
- All code files will be executed on Ubuntu 18.04 LTS with Python 3.7.
- Code should follow the `pycodestyle` style guide (version 2.5).
- Each module, class, and function should have docstrings describing their purpose.
- All code must be type-annotated.
- A `README.md` file at the project root is mandatory.

## Resources
- [unittest — Unit testing framework](https://docs.python.org/3/library/unittest.html)
- [unittest.mock — mock object library](https://docs.python.org/3/library/unittest.mock.html)
- [parameterized](https://pypi.org/project/parameterized/)
- [Memoization](https://en.wikipedia.org/wiki/Memoization)

## Installation

Ensure `unittest` and `parameterized` are available in your Python environment. To install `parameterized`, run:
```bash
pip install parameterized
```

## Testing Commands

To run a test file:
```bash
python -m unittest path/to/test_file.py
```

## Project Structure

The project is divided into unit and integration tests. Each test class targets a specific function or class, with parameters and mock setups tailored to each testing scenario.

### Directory Structure

```
.
├── test_client.py           # Integration tests for GithubOrgClient
├── test_utils.py            # Unit tests for utility functions
└── README.md                # Project documentation
```

## Tasks

### Task 0-1: Parameterize a Unit Test

Test the function `utils.access_nested_map`, ensuring it correctly handles valid and invalid paths within nested dictionaries. We will also parameterize these tests to handle multiple input cases, and test for `KeyError` exceptions when invalid paths are provided.

### Task 2: Mock HTTP Calls

Mock HTTP calls in the `utils.get_json` function to avoid external requests during testing. Patch `requests.get` to return a mock JSON response and validate that the function produces the expected output.

### Task 3: Parameterize and Patch

Implement tests for the `utils.memoize` decorator by defining a test class that validates the decorator’s memoization functionality. Mock specific methods to ensure a method is only called once even when accessed multiple times through a property.

### Task 4-7: GithubOrgClient Unit Tests

Create unit tests for `GithubOrgClient` class methods:
- **test_org**: Test `GithubOrgClient.org` using mock and parameterized inputs.
- **test_public_repos_url**: Mock `GithubOrgClient.org` and validate that `_public_repos_url` returns the correct URL.
- **test_public_repos**: Mock `get_json` and `_public_repos_url` to verify the functionality of `public_repos`.
- **test_has_license**: Verify that `has_license` correctly identifies repositories with a specified license.

### Task 8-9: Integration Tests

In `TestIntegrationGithubOrgClient`, use fixtures for end-to-end tests of `GithubOrgClient.public_repos`. Mock `requests.get` using `setUpClass` to load different response payloads for URLs, and ensure the correct list of repositories is returned based on the specified license.

## How to Run Tests

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/alx-backend-python
   ```
2. Navigate to the project directory:
   ```bash
   cd alx-backend-python/0x03-Unittests_and_integration_tests
   ```
3. Run all tests:
   ```bash
   python -m unittest discover .
   ```

## Author
**Abdelrhman Fikri**
