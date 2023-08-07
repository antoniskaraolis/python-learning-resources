# Python Beginner's Exercises and Solutions


## Variables and Data Types

**Exercise:** Define a string, integer, float, and boolean variable. Print the type of each variable.

**Solution:**
```python
string_var = "Hello, world!"
int_var = 10
float_var = 10.5
boolean_var = True

print(type(string_var))  # <class 'str'>
print(type(int_var))  # <class 'int'>
print(type(float_var))  # <class 'float'>
print(type(boolean_var))  # <class 'bool'>
```

## Basic Operators

**Exercise:** Perform arithmetic operations: addition, subtraction, multiplication, and division between two numbers.

**Solution:**
```python
a = 10
b = 5

print(a + b)  # 15
print(a - b)  # 5
print(a * b)  # 50
print(a / b)  # 2.0
```

## Lists

**Exercise:** Create a list, append an element to it, remove an element from it, and print the length of the list.

**Solution:**
```python
my_list = [1, 2, 3]
my_list.append(4)  # my_list is now [1, 2, 3, 4]
my_list.remove(2)  # my_list is now [1, 3, 4]
print(len(my_list))  # 3
```

## Dictionaries

**Exercise:** Create a dictionary, add a key-value pair to it, remove a key-value pair from it, and print the dictionary.

**Solution:**
```python
my_dict = {'a': 1, 'b': 2}
my_dict['c'] = 3  # my_dict is now {'a': 1, 'b': 2, 'c': 3}
del my_dict['a']  # my_dict is now {'b': 2, 'c': 3}
print(my_dict)  # {'b': 2, 'c': 3}
```

## Control Flow

**Exercise:** Write a Python program to find the largest number among three numbers using an if-elif-else statement.

**Solution:**
```python
num1 = 10
num2 = 15
num3 = 12

if (num1 >= num2) and (num1 >= num3):
   largest = num1
elif (num2 >= num1) and (num2 >= num3):
   largest = num2
else:
   largest = num3

print("The largest number is", largest)  # The largest number is 15
```

## Functions

**Exercise:** Define a function that calculates the factorial of a number.

**Solution:**
```python
def factorial(n):
   if n == 0:
       return 1
   else:
       return n * factorial(n-1)

print(factorial(5))  # 120
```

## Classes and Objects

**Exercise:** Create a class named *Rectangle with two attributes *length and *width. Add two methods: `area()` and `perimeter()`, which calculate the area and perimeter of the rectangle respectively.

**Solution:**
```python
class Rectangle:
   def __init__(self, length, width):
       self.length = length
       self.width = width

   def area(self):
       return self.length * self.width

   def perimeter(self):
       return 2 * (self.length + self.width)

rectangle = Rectangle(4, 7)
print(rectangle.area())  # 28
print(rectangle.perimeter())  # 22
```

## Error Handling

**Exercise:** Write a Python program that asks the user for an integer input and uses error handling to avoid a ValueError if the user does not provide an integer.

**Solution:**
```python
try:
    user_input = int(input("Please enter an integer: "))
except ValueError:
    print("That's not an integer!")
```

## File I/O

**Exercise:** Write a Python program that writes a sentence to a file and then reads the file to print its content.

**Solution:**
```python
with open('test.txt', 'w') as file:
    file.write("Hello, world!")

with open('test.txt', 'r') as file:
    print(file.read())  # Hello, world!
```
