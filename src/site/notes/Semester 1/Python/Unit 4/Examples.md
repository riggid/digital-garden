---
{"dg-publish":true,"permalink":"/semester-1/python/unit-4/examples/"}
---


# [Back](../../Python.md)
***
[Core Notes](Core%20Notes.md) | [Examples](Examples.md) | [Questions](Questions.md)

# Unit 4 Examples

## Example 1: Map and Filter with Lambda
```python
nums = [1, 2, 3, 4, 5, 6]

# Square even numbers
evens = filter(lambda x: x % 2 == 0, nums)
squared_evens = map(lambda x: x**2, evens)

print(list(squared_evens)) # [4, 16, 36]
```

## Example 2: Operator Overloading
```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)

    def __str__(self):
        return f"Vector({self.x}, {self.y})"

v1 = Vector(1, 2)
v2 = Vector(3, 4)
v3 = v1 + v2
print(v3) # Vector(4, 6)
```

## Example 3: Inheritance
```python
class Animal:
    def speak(self):
        print("Generic Sound")

class Dog(Animal):
    def speak(self):
        print("Woof")

class Cat(Animal):
    def speak(self):
        print("Meow")

animals = [Dog(), Cat(), Animal()]
for a in animals:
    a.speak()
# Output:
# Woof
# Meow
# Generic Sound
```

## Example 4: Custom Iterator
```python
class CountDown:
    def __init__(self, start):
        self.current = start

    def __iter__(self):
        return self

    def __next__(self):
        if self.current <= 0:
            raise StopIteration
        val = self.current
        self.current -= 1
        return val

for num in CountDown(3):
    print(num)
# 3
# 2
# 1
```
