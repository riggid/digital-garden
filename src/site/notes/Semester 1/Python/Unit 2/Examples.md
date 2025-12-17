---
{"dg-publish":true,"permalink":"/semester-1/python/unit-2/examples/"}
---


# [[../../Python\|Back]]
***
[[Semester 1/Python/Unit 2/Core Notes\|Core Notes]] | [[Semester 1/Python/Unit 2/Examples\|Examples]] | [[Semester 1/Python/Unit 2/Questions\|Questions]]

# Unit 2 Examples

## Example 1: List Operations
```python
# List creation
numbers = [10, 20, 30, 40, 50]

# Accessing
print(numbers[0])    # 10
print(numbers[-1])   # 50 (Last element)

# Slicing
print(numbers[1:4])  # [20, 30, 40]
print(numbers[::-1]) # [50, 40, 30, 20, 10] (Reverse)

# Modification
numbers[2] = 99
print(numbers)       # [10, 20, 99, 40, 50]

# Methods
numbers.append(60)
numbers.insert(0, 5)
numbers.pop()        # Removes 60
print(numbers.count(20)) # 1
```

## Example 2: Tuple Packing and Unpacking
```python
t = (1, 2, "Hello")

# Unpacking
a, b, c = t
print(a) # 1
print(c) # Hello

# Swaping variables
x = 5
y = 10
x, y = y, x
print(x, y) # 10 5
```

## Example 3: Function with *args and **kwargs
```python
def flexible_function(*args, **kwargs):
    print("Positional arguments (tuple):", args)
    print("Keyword arguments (dict):", kwargs)

flexible_function(1, 2, 3, name="Alice", age=25)

# Output:
# Positional arguments (tuple): (1, 2, 3)
# Keyword arguments (dict): {'name': 'Alice', 'age': 25}
```

## Example 4: Local vs Global Scope
```python
x = 10 # Global

def modify():
    global x
    x = 20 # Modifies global x

modify()
print(x) # 20
```
