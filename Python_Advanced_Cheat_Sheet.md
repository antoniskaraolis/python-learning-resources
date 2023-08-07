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
