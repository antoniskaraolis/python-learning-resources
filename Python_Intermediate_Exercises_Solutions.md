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





