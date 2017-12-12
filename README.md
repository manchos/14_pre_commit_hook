# Quadratic Equations Solver

This program calculate roots of quadratic equation and start tests (test.py) in case commiting.


The get_roots function is tested.
If you need to modify the function and want to check it before each commit you can put put pre-commit file to .git\hooks
The commit will be done only if all tests work properly. Otherwise an error message will be shown

# Usage
The example shows that in the current form `quadratic_equation.py` does not comply with our tests and an error occur when trying to commit.
```#!bash
$ git commit -m "initial commit"
.E..
======================================================================
ERROR: test_returns_none_for_complex_solution (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 22, in test_returns_none_for_complex_solution
    root1, root2 = get_roots(1, 2, 3)
  File "/Users/anyya/python/devman/14_pre_commit_hook/quadratic_equation.py", line 5, in get_roots
    root1 = (-b - sqrt(discriminant)) / (2 * a)
ValueError: math domain error

----------------------------------------------------------------------
Ran 4 tests in 0.002s

FAILED (errors=1)
> Failed! Fix your code and run tests before commit.

```

## Example of broken code detection

# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
