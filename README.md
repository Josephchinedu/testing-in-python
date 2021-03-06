# testing-in-python

## unittest
unittest has been built into the Python standard library since version 2.1<br />
unittest contains both a testing framework and a test runner. unittest has some important requirements for writing and executing tests.
```python

import unittest

class TestSum(unittest.TestCase):
    def test_sum(self):
        self.assertEqual(sum([1,2,3]), 6, "answer should be 6")

    def test_sum_tuple(self):
        self.assertEqual(sum((1,2,3)), 6, "answer should be 6")


if __name__ == "__main__":
    unittest.main()

```

## nose
You may find that over time, as you write hundreds or even thousands of tests for your application, <br /> it becomes increasingly hard to understand and use the output from unittest.<br />
nose is compatible with any tests written using the unittest framework and can be used as a drop-in replacement for the unittest test runner.<br />
To get started with nose2, install nose2 from PyPI and execute it on the command line.
```bash
pip install nose2

```
run nose 
```python
python -m nose2
```


## pytest
pytest supports execution of unittest test cases. The real advantage of pytest comes by <br /> writing pytest test cases. pytest test cases are a series of functions in a Python file starting<br /> with the name test_.<br />
Writing the TestSum test case example for pytest would look like this:

##### create a file "test_sum.py"
install pytest

```bash

pip insatll pytest

```

script
```python

def test_sum():
    assert sum([1, 2, 3]) == 6, "answer should be 6"
        
def test_sum_tuple():
    assert sum((1, 2, 2)) == 5, "answer should be 5"


```
run a test.

```bash
pytest

```
``` More information can be found at the Pytest ``` [Documentation Website.](https://docs.pytest.org/en/latest/)

