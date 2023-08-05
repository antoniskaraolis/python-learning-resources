# Python Beginner's Cheat Sheet

## Variables and Data Types

```python
int_var = 10    # Integer
float_var = 10.5    # Float
string_var = "Hello, world!"    # String
boolean_var = True    # Boolean
```

## Basic Operators

```python
# Arithmetic
add = 5 + 5    # Addition
sub = 5 - 2    # Subtraction
mul = 3 * 3    # Multiplication
div = 10 / 2    # Division
mod = 10 % 3    # Modulus
exp = 2 ** 3    # Exponentiation

# Comparison
eq = 5 == 5    # Equal
ne = 5 != 5    # Not equal
gt = 5 > 3    # Greater than
lt = 3 < 5    # Less than
ge = 5 >= 5    # Greater than or equal to
le = 3 <= 5    # Less than or equal to
```
## Lists

```python
my_list = [1, 2, 3, 4, 5]    # Create list
my_list.append(6)    # Append to list
my_list.remove(1)    # Remove from list
```
## Dictionaries

```python
my_dict = {'key': 'value'}    # Create dictionary
my_dict['new_key'] = 'new_value'    # Add to dictionary
del my_dict['key']    # Remove from dictionary
```
## Control Flow

```python
# If statement
if condition:
    # Do something
elif other_condition:
    # Do something else
else:
    # Do another thing

# For loop
for i in range(5):
    # Do something

# While loop
while condition:
    # Do something
```

def my_function(param1, param2):
    # Do something
    return result

class MyClass:
    def __init__(self, param1, param2):
        self.param1 = param1
        self.param2 = param2

    def my_method(self):
        # Do something

my_object = MyClass('value1', 'value2')    # Create object
my_object.my_method()    # Call method

try:
    # Do something
except Exception as e:
    # Handle exception
finally:
    # Execute cleanup code

with open('myfile.txt', 'r') as file:
    content = file.read()    # Read file

with open('myfile.txt', 'w') as file:
    file.write('Hello, world!')    # Write to file



Please remember that this cheat sheet covers only the very basics of Python. Python is a vast language with many built-in features and third-party libraries. You will continue learning more about Python as you gain more experience and work on more projects.
