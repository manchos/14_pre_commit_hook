# Quadratic Equations Solver

This program calculates roots of quadratic equation and uses git hook pre-commit for autorun unit tests.
The arguments a, b, and c are the coefficients of the equation.

# Pre-commit hook

Copy file pre-commit into dir .../our_project/.git/hooks

check script

```bash
$ cp pre-commit .../our_project/.git/hooks
$ chmod +x .../our_project/.git/hooks/pre-commit

```

After that tests will be run automatically when you try to commit. If tests fail commit will be aborted.

# Usage

```bash
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

# Tests
Module tests.py contains unit tests. You can run it by typing:

```#!bash

$ python tests.py
```

# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
