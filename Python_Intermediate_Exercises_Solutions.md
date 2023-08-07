# Python Intermediate Exercises and Solutions

## List Comprehensions

**Exercise:** Use a list comprehension to create a list of squares of numbers from 1 to 10.

**Solution:**
```python
squares = [n**2 for n in range(1, 11)]
print(squares)  # Output: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

## Dictionary Comprehensions

**Exercise:** Use a dictionary comprehension to create a dictionary mapping numbers from 1 to 5 to their squares.

**Solution:**
```python
square_dict = {n: n**2 for n in range(1, 6)}
print(square_dict)  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

## Set Comprehensions

**Exercise:** Use a set comprehension to create a set of squares of numbers from -5 to 5.

**Solution:**
```python
unique_squares = {n**2 for n in range(-5, 6)}
print(unique_squares)  # Output: {0, 1, 4, 9, 16, 25}
```

## Generators

**Exercise:** Create a generator that yields the Fibonacci sequence.

**Solution:**
```python
def fibonacci():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b

fib = fibonacci()
for _ in range(10):
    print(next(fib))  # Outputs the first 10 numbers of the Fibonacci sequence
```

## Decorators

**Exercise:** Create a decorator that prints the execution time of a function.

**Solution:**
```python
import time

def timer_decorator(func):
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"Execution time: {end - start} seconds")
        return result
    return wrapper

@timer_decorator
def delay(seconds):
    time.sleep(seconds)

delay(5)  # Sleeps for 5 seconds, then prints the execution time
```

## Error Handling with else and finally

**Exercise:** Write a function that asks the user for an integer input, uses a try/except block to catch `ValueError` exceptions, uses an `else` clause to print the number if no exception was raised, and a `finally` clause to print "End of function".

**Solution:**
```python
def get_number():
    try:
        number = int(input("Enter an integer: "))
    except ValueError:
        print("That's not an integer!")
    else:
        print(f"You entered {number}")
    finally:
        print("End of function")

get_number()
```

## Using *args and **kwargs

**Exercise:** Write a function that accepts any number of positional and keyword arguments, and prints them.

**Solution:**
```python
def print_args(*args, **kwargs):
    for arg in args:
        print(arg)
    for key, value in kwargs.items():
        print(f"{key} = {value}")

print_args(1, 2, 3, a=4, b=5)
```

## Working with Files

**Exercise:** Write a program that creates a text file, writes a few lines to it, then reads the file and prints its contents.

**Solution:**
```python
with open('myfile.txt', 'w') as file:
    file.write("Hello, world!\n")
    file.write("How are you?")

with open('myfile.txt', 'r') as file:
    print(file.read())  # Prints: Hello, world! How are you?
```

## Lambda Functions

**Exercise:** Write a lambda function that adds two numbers and call it with the numbers 3 and 5.

**Solution:**
```python
add = lambda x, y: x + y
print(add(3, 5))  # Output: 8
```

## Using map, filter, and reduce

**Exercise:** Use map to double the numbers in a list, filter to select only the numbers greater than 10, and reduce to find the product of the numbers.

**Solution:**
```python
from functools import reduce

numbers = [1, 2, 3, 4, 5]
doubled = list(map(lambda x: x * 2, numbers))
greater_than_ten = list(filter(lambda x: x > 10, doubled))
product = reduce(lambda x, y: x * y, greater_than_ten)
print(product)  # Output: 480
```

## Working with Modules and Packages

**Exercise:** Use the math module to calculate the square root, cosine, and logarithm of a number.

**Solution:**
```python
import math

number = 100
print(math.sqrt(number))  # Output: 10.0
print(math.cos(number))  # Output: 0.8623188722876839
print(math.log(number))  # Output: 4.605170185988092
```

## Working with Iterators and Generators

**Exercise:** Create an iterator class that iterates from 1 up to a number **`n`**.

**Solution:**
```python
class MyIterator:
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

my_iterator = MyIterator(5)
for i in my_iterator:
    print(i)  # Output: 1 2 3 4 5
```

