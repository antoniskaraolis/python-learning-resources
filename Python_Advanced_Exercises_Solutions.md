# Python Advanced Exercises and Solutions

## Advanced List Comprehensions

**Exercise:** Use a list comprehension to create a list of the squares of odd numbers from 1 to 10.

**Solution:**
```python
squares = [n**2 for n in range(1, 11) if n % 2 != 0]
print(squares)  # Output: [1, 9, 25, 49, 81]
```

## Advanced Dictionary Comprehensions

**Exercise:** Use a dictionary comprehension to create a dictionary mapping odd numbers from 1 to 5 to their squares.

**Solution:**
```python
square_dict = {n: n**2 for n in range(1, 6) if n % 2 != 0}
print(square_dict)  # Output: {1: 1, 3: 9, 5: 25}
```

## Context Managers

**Exercise:** Use a context manager to open a file and write the string 'Hello, world!' to it.

**Solution:**
```python
with open('hello.txt', 'w') as file:
    file.write("Hello, world!")
```

## Generators with Expressions

**Exercise:** Use a generator expression to create a generator that yields the squares of numbers from 1 to 10.

**Solution:**
```python
squares = (n**2 for n in range(1, 11))
for square in squares:
    print(square)
```

## Decorators with Arguments

**Exercise:** Create a decorator that repeats the execution of a function a given number of times.

**Solution:**
```python
def repeat(num_times):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(num_times):
                func(*args, **kwargs)
        return wrapper
    return decorator

@repeat(3)
def greet():
    print("Hello!")

greet()  # Prints "Hello!" three times
```

## Error Handling with Custom Exceptions

**Exercise:** Create a custom exception called **`MyError`** and write a function that raises this exception when called with the argument 'error'.

**Solution:**
```python
class MyError(Exception):
    pass

def trigger_error(message):
    if message == 'error':
        raise MyError('Error triggered!')

try:
    trigger_error('error')
except MyError as e:
    print(e)  # Output: Error triggered!
```

## Advanced Object-Oriented Programming

**Exercise:** Create a class **'Dog'** that inherits from a class **'Animal'** and overrides a method **'speak'**.

**Solution:**
```python
class Animal:
    def speak(self):
        return "Animal speaks..."

class Dog(Animal):
    def speak(self):
        return "Woof!"

dog = Dog()
print(dog.speak())  # Output: Woof!
```

## Magic Methods and Operator Overloading

**Exercise:** Create a class **'Vector'** that supports addition and subtraction with other vectors using operator overloading.

**Solution:**
```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

    def __sub__(self, other):
        return Vector(self.x - other.x, self.y - other.y)

    def __str__(self):
        return f"Vector({self.x}, {self.y})"

v1 = Vector(1, 2)
v2 = Vector(2, 3)
print(v1 + v2)  # Output: Vector(3, 5)
print(v1 - v2)  # Output: Vector(-1, -1)
```

## Advanced Iterators and Generators

**Exercise:** Create an iterator class **'Counter'** that iterates from 1 up to a number **'n'**.

**Solution:**
```python
class Counter:
    def __init__(self, n):
        self.n = n
        self.i = 1

    def __iter__(self):
        return self

    def __next__(self):
        if self.i <= self.n:
            i = self.i
            self.i += 1
            return i
        else:
            raise StopIteration

for number in Counter(5):
    print(number)  # Output: 1 2 3 4 5
```

## Metaclasses

**Exercise:** Create a metaclass **'Meta'** that adds a method **'hello'** to the classes it creates.

**Solution:**
```python
class Meta(type):
    def __init__(cls, name, bases, attrs):
        attrs['hello'] = lambda self: 'Hello, world!'
        super().__init__(name, bases, attrs)

class MyClass(metaclass=Meta):
    pass

print(MyClass().hello())  # Output: Hello, world!
```

## Asynchronous Programming

**Exercise:** Use the `asyncio` module to write a program that fetches the content of a URL.

**Solution:**
```python
import aiohttp
import asyncio

async def fetch(session, url):
    async with session.get(url) as response:
        return await response.text()

async def main():
    async with aiohttp.ClientSession() as session:
        html = await fetch(session, 'http://python.org')
        print(html)

asyncio.run(main())
```


