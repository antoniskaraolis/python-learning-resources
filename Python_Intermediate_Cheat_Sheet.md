# Python Intermediate Cheat Sheet

## List Comprehensions

List comprehensions provide a concise way to create lists based on existing lists. 

```python
# Squaring each element in a list
numbers = [1, 2, 3, 4, 5]
squares = [n**2 for n in numbers]  # Output: [1, 4, 9, 16, 25]
```

## Dictionary Comprehensions

Dictionary comprehensions allow you to express creation of dictionaries using a similar concise syntax.

```python
# Creating a dictionary mapping numbers to their squares
numbers = [1, 2, 3, 4, 5]
square_dict = {n: n**2 for n in numbers}  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

## Set Comprehensions

Set comprehensions allow you to create sets using a similar syntax to list comprehensions.

```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5]
unique_squares = {n**2 for n in numbers}  # Output: {1, 4, 9, 16, 25}
```

## Generators

Generators are a special type of iterable defined using a function rather than being stored in memory.

```python
# Generator for square numbers
def squares(n):
    for i in range(n):
        yield i**2

squares_generator = squares(10)  # Use the generator
```

## Decorators

Decorators allow you to wrap a function with another function to extend its functionality.

```python
def my_decorator(func):
    def wrapper(*args, **kwargs):
        print("Before function call")
        result = func(*args, **kwargs)
        print("After function call")
        return result
    return wrapper

@my_decorator
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")
```

## Error Handlign with else and finally

`else` in error handling is used when you want to check if there was no exception in the `try` block. `finally` is always executed regardless of whether an exception occurred or not.

```python
try:
    # Code that might raise an error
    x = 1 / 1
except ZeroDivisionError:
    # Code to run if a ZeroDivisionError occurs
    print("You tried to divide by zero!")
else:
    # Code to run if no error occurs
    print("No errors occurred!")
finally:
    # Code to run no matter what happens
    print("Cleaning up...")
```

## Using *args and **kwargs

`*args` and `**kwargs` allow you to pass a variable number of arguments to a function.

```python
def example_function(*args, **kwargs):
    for arg in args:
        print(f"Argument: {arg}")
    for key, value in kwargs.items():
        print(f"Keyword argument: {key} = {value}")

example_function(1, 2, 3, a=4, b=5)
```

## Working with Files

Python allows you to read from and write to files on your system.

```python
# Read a file line by line
with open('myfile.txt', 'r') as file:
    for line in file:
        print(line)

# Write to a file
with open('myfile.txt', 'w') as file:
    file.write('Hello, world!')
```

## Lambda Functions

Lambda functions are small anonymous functions defined using the `lambda` keyword.

```python
square = lambda x: x**2
print(square(5))  # Output: 25
```

## Using map, filter, and reduce

`map`, `filter`, and `reduce` are built-in Python functions that operate on lists (and other iterables).

```python
from functools import reduce

numbers = [1, 2, 3, 4, 5]

# Use map to square all numbers in the list
squared = list(map(lambda x: x**2, numbers))

# Use filter to get all numbers in the list that are larger than 2
greater_than_two = list(filter(lambda x: x > 2, numbers))

# Use reduce to get the product of all numbers in the list
product_of_all = reduce(lambda x, y: x * y, numbers)
```

## Working with Modules and Packages

Python allows you to organize your code into modules and packages. You can import functions, classes, and variables from them into your code.

```python
# Importing a built-in module
import math

# Importing a third-party module with an alias
import numpy as np

# Importing a specific function from a module
from math import sqrt
```

## Working with Iterators and Generators

Iterators and generators are powerful tools for working with sequences of values.

```python
# Creating an iterator
class MyIterator:
    def __init__(self, start, end):
        self.value = start
        self.end = end

    def __iter__(self):
        return self

    def __next__(self):
        if self.value >= self.end:
            raise StopIteration
        current_value = self.value
        self.value += 1
        return current_value
```



















































