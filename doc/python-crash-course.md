# Python Crash Course, 3rd Ed.

Following *Python Crash Course, 3rd Ed.* to learn Python.

## Introduction

## Part I: Basics

### Chapter 1: Getting Started

Write a short "hello world" program and have it run in VS Code.  (After selecting a Python interpreter, go to `Run > Run Without Debugging`)

### Chapter 2: Variables and Simple Data Types

Variables are mutable.  Don't need to have type explicitly defined.

General rules for Python variable naming:
- Variable names can contain only letters, numbers, and underscores.
- Variable names can't start with a number.
- Avoid Python keywords and function names as variable names.

#### Strings

A string is a series of characters.

Anything inside quotes is considered a string in Python.

You can use single or double quotes around your strings.

```python
"This is a string."
'This is also a string.'
```

Strings are objects that have methods.

Methods are actions that can be performed on a piece of data.

If `name = "ada lovelace"` is a string variable, then `name.title() == "Ada Lovelace"`.  That is, `title()` is a method that returns the string in title case.

All methods require parentheses after their name, but can be empty.


### Other chapters

### Chapter 9: Classes

### Creating and Using a Class

Python files are modules.  Classes can be defined in modules (maybe elsewhere?).  Example:

```python
class Dog:
    """A simple attempt to model a dog."""

    def __init__(self, name, age):
        """Initialize name and age attributes"""
        self.name = name
        self.age = age

    def sit(self):
        """Simulate a dog sitting in response to a command."""
        print(f"{self.name} is now sitting.")

    def roll_over(self):
        """Simulate rolling over in response to a command."""
        print(f"{self.name} rolled over!")
```
