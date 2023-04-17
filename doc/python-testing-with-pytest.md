# Python Testing with pytest (Feb 2022)

Book was written by Brian Okken.

## Preface

### Why pytest?

pytest is a software testing framework, which means pytest is:
- a command-line tool that automatically finds tests you've written
- runs the tests
- reports the results

Also, it can be extended by writing plugins or installing third-party plugins, and integrates well with CI/CD/automation tools.

## Part I. Primary Power

### 1. Getting Started with pytest

#### Installing pytest

Recommendation for starting a Python virtual environment in Linux and installing pytest

```bash
$ python3 -m venv venv
$ source venv/bin/activate
(venv) $ pip install pytest
```

#### Running pytest

At terminal:

```bash
​$ ​​pytest​​ ​​test_one.py​
​ 	========================= test session starts ==========================
​ 	collected 1 item
​ 	
​ 	test_one.py .                                                    [100%]
​ 	
​ 	========================== 1 passed in 0.01s ===========================
```

Passing `-v` or `--verbose` parameter will provide verbose output. Can give good information about exactly how the output and expected output are different.

`--tb=no` flag will turn off tracebacks.

Can specify files individually or by directory

```bash
pytest --tb=no test_one.py test_two.py
```
or
```bash
pytest --tb=no src/testing-with-pytest/ch1
```
Can also specify individual functions to be tested:
```bash
pytest --tb=no src/testing-with-pytest/ch1/test_one.py::test_passing
```

##### Test discovery

Given no arguments, pytest looks at your current directory and all subdirectories for test files and runs the test code it finds.
If you give pytest a filename, a directory name, or a list of those, it looks there instead of the current directory.
Each directory listed on the command line is examined for test code, as well as any subdirectories.

Here are the naming conventions to keep test code discoverable by pytest:
- Test files should be named `test_<something>.py` or `<something>_test.py`.
- Test methods and functions should be named `test_<something>`.
- Test classes should be named `Test<Something>`.

Configuration files can be used to alter the discovery rules.

##### Test Outcomes

Possible outcomes:
- PASSED (.)
- FAILED (F)
- SKIPPED (s)
- XFAIL (x) -- the test not supposed to pass, and it ran and failed
- XPASS (X) -- the test was marked with xfail, but it ran and passed
- ERROR (E) -- an error with execution of a fixture or hook function, not within the test function

## Other parts

## Appendices

### Appendix 1: Virtual Environments

Many reasons to use virtual environments.
- Multiple services running with the same Python installation, but with different packages and package version requirements
- Can keep the dependent package requirements separate for every Python project you work on.

`venv` is the virtual environment module included as part of the standard library.

If `venv` causes any issues, use `virtualenv` instead (install with `pip install virtualenv`).

Basic workflow for using `venv`:
- Create
    - `python -m venv env_dir_name [--prompt my_proj]`
- Activate
    - `source env_dir_name/bin/activate` to activate on Linux
- Deactivate
    - `deactivate` when done

Can use any directory name, but `venv` or `.venv` is customary. `prompt` parameter is optional.

The end.
