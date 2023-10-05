# 0x00-python_variable_annotations

# Concepts

For this project, we expect you to look at this concept:

1. Advanced Python

* Python is a dynamically-typed language. That means that variable types are dynamically set at run-time, upon assignment of a value to a variable.

* For example, in

```
def fn(a, b):
    return a + b
```

The types of a and b are not known at build-time, only when a and b are assigned values at run-time.

Hence, calling

```
fn("a", 1)
```

somewhere in your code will not raise an exception until the code is actually executed and the function is called:

```
>>> fn("a", 1)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

In Python 3, type annotations do not change this. Python is still a dynamically-typed language. Type annotations serve the following purpose:

* Code documentation: thanks to them, a developer reading type-annotated code (his own or someone else’s) will know exactly what type each variables is supposed to be. This helps reduce bugs and exceptions and accelerate the development cycle.
* Linting and validation: code editors and continuous integration (CI) pipelines can be configured to automatically validate type-annotated code at build-time and catch bugs before they make it to production.


# Resources

## Read or watch:

* [Python 3 typing documentation](https://docs.python.org/3/library/typing.html)
* [MyPy cheat sheet](https://mypy.readthedocs.io/en/latest/cheat_sheet_py3.html)

## Learning Objectives

### General

At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

* Type annotations in Python 3
* How you can use type annotations to specify function signatures and variable types
* Duck typing
* How to validate your code with mypy