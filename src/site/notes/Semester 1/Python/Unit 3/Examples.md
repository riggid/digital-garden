---
{"dg-publish":true,"permalink":"/semester-1/python/unit-3/examples/"}
---


# [[../../Python\|Back]]
***
[[Semester 1/Python/Unit 3/Core Notes\|Core Notes]] | [[Semester 1/Python/Unit 3/Examples\|Examples]] | [[Semester 1/Python/Unit 3/Questions\|Questions]]

# Unit 3 Examples

## Example 1: Recursive Factorial
```python
def factorial(n):
    # Base Case
    if n == 0 or n == 1:
        return 1
    # Recursive Case
    return n * factorial(n - 1)

print(factorial(5)) # 120
```

## Example 2: Callback with Sort
```python
words = ["apple", "Banana", "cherry", "Date"]

# Sort case-insensitive using a callback
def ignore_case(s):
    return s.lower()

words.sort(key=ignore_case)
# Equivalent lambda: words.sort(key=lambda s: s.lower())

print(words) # ['apple', 'Banana', 'cherry', 'Date']
```

## Example 3: Doctest
```python
def add(a, b):
    """
    Returns the sum of a and b.
    >>> add(2, 3)
    5
    >>> add(-1, 1)
    0
    """
    return a + b

if __name__ == "__main__":
    import doctest
    doctest.testmod()
```

## Example 4: Basic Tkinter Window
```python
import tkinter as tk

def on_click():
    label.config(text="Button Clicked!")

root = tk.Tk()
root.title("My App")

label = tk.Label(root, text="Hello GUI")
label.pack()

btn = tk.Button(root, text="Click Me", command=on_click)
btn.pack()

root.mainloop()
```
