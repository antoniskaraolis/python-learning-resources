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
















