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

Passing `-v` or `--verbose` parameter will provide verbose output.

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
