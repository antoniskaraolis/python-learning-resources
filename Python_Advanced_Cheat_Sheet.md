# Python Advanced Cheat Sheet

## Advanced List Comprehensions

List comprehensions can include conditions and multiple inputs.

```python
# List comprehension with if condition
evens = [x for x in range(10) if x % 2 == 0]

# Nested list comprehension
flattened = [item for sublist in nested_list for item in sublist]
```

## Advanced Dictionary Comprehensions

Dictionary comprehensions can also include conditions and multiple inputs.

```python
# Dictionary comprehension with if condition
even_square_dict = {x: x**2 for x in range(10) if x % 2 == 0}
```

## Context Managers

Context managers automate setup and teardown activities, commonly used with file operations and database connections.

```python
# Using a context manager to work with files
with open('file.txt', 'r') as file:
    contents = file.read()
```

## Generators with Expressions

You can create compact generator objects with generator expressions (similar to list comprehensions).

```python
# Generator expression
gen = (x**2 for x in range(10))
```

## Decorators with Arguments

Decorators can accept arguments, which requires an additional level of nesting.

```python
# Decorator with arguments
def repeat(num_times):
    def decorator_repeat(func):
        def wrapper(*args, **kwargs):
            for _ in range(num_times):
                func(*args, **kwargs)
        return wrapper
    return decorator_repeat

@repeat(num_times=4)
def greet(name):
    print(f"Hello {name}")

greet("Alice")
```

## Error Handling with Custom Exceptions

You can define custom exception types for your program.

```python
# Custom exception
class CustomError(Exception):
    pass

try:
    raise CustomError("This is a custom error")
except CustomError as e:
    print(e)
```

## Object-Oriented Programming (OOP)

Python supports advanced OOP features like inheritance, encapsulation, and polymorphism.

```python
# Inheritance in Python
class Animal:
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"
```

## Magic Methods and Operator Overloading

Magic methods let you define custom behavior for built-in Python operations.

```python
# Custom string representation of a class
class MyClass:
    def __init__(self, name):
        self.name = name

    def __repr__(self):
        return f"MyClass(name={self.name})"

    def __str__(self):
        return self.name

my_obj = MyClass("Example")
print(repr(my_obj))  # MyClass(name=Example)
print(str(my_obj))  # Example
```

## Iterators and Generators

Understanding the internals of Python's iterator and generator system.

```python
# A custom iterator
class Counter:
    def __init__(self, low, high):
        self.current = low
        self.high = high

    def __iter__(self):
        return self

    def __next__(self):
        if self.current > self.high:
            raise StopIteration
        else:
            self.current += 1
            return self.current - 1

for number in Counter(3, 8):
    print(number)
```

## Metaclasses

Metaclasses are the 'classes' of classes, allowing for class-level programming.

```python
# Simple metaclass
class Meta(type):
    def __new__(cls, name, bases, dct):
        x = super().__new__(cls, name, bases, dct)
        x.attr = 100
        return x

class MyClass(metaclass=Meta):
    pass

print(MyClass.attr)  # 100
```

## Asynchronous Programming

Python's **`asyncio`** module allows for asynchronous I/O operations, and is particularly useful for high-performance network and server applications.

```python
# Asynchronous programming with asyncio
import asyncio

async def main():
    print('Hello')
    await asyncio.sleep(1)
    print('World')

asyncio.run(main())
```

**This is a non-exhaustive list of advanced Python topics, but it should give you a good idea of the power and flexibility that Python provides.**

