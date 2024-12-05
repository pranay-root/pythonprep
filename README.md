#Introduction 

```markdown
# Introduction to Python

## What is Python?
Python is a popular programming language created by **Guido van Rossum** and released in **1991**.

### Applications of Python:
1. **Web development** (server-side)
2. **Software development**
3. **Mathematics**
4. **System scripting**

---

## Syntax

### Conditional Statements
```python
if a > b:  # Condition is true, so the indented code will execute
    print("a is greater than b")

if 5 < 3:  # Condition is false, so the indented code will not execute
    print("This will not be printed.")
```

---

## Variables

- Variables are containers for storing data values.
- A variable is created the moment you assign a value to it.
- **Variable names are case-sensitive.**

### Example:
```python
x = 5
y = "Hello, World!"
```

### Casting Variables:
```python
x = int(5)        # Integer
y = str("hello")  # String
z = float(3)      # Float
```

---

## Comments

- **Single-line comment:** Use `#`  
```python
# This is a single-line comment
```

- **Multi-line comment:** Use triple quotes (`"""`)
```python
"""
This is
a multi-line comment
"""
```

---

## `type()` Function

- The `type()` function is used to print the type of a variable.
- **Syntax:**
```python
x = 5
print(type(x))  # Output: <class 'int'>
```

---

## Variable Names

### Rules for Naming Variables:
1. A variable name **must start** with a letter or an underscore (`_`).
2. A variable name **cannot start** with a number.
3. A variable name can only contain **alpha-numeric characters** and underscores (`A-z`, `0-9`, `_`).
4. Variable names are **case-sensitive** (e.g., `age`, `Age`, and `AGE` are different).
5. A variable name **cannot** be any of Python's reserved keywords.

### Examples:
```python
# Many values to multiple variables:
x, y, z = "Orange", "Banana", "Cherry"

# One value to multiple variables:
x = y = z = "Orange"

# Unpacking a collection:
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
```

---

## Global Variables

- **Global variables** are defined outside any function and can be accessed both **inside** and **outside** functions.

### Example:
```python
x = "awesome"

def myfunc():
    print("Python is " + x)

myfunc()
```

---

## Local Variables

- **Local variables** are defined inside a function and can only be accessed within that function.

### Example:
```python
x = "awesome"

def myfunc():
    x = "fantastic"  # Local variable
    print("Python is " + x)

myfunc()

print("Python is " + x)  # Uses the global variable
```

---

## `global` Keyword

- The `global` keyword allows you to define or modify a **global variable** inside a function.

### Syntax:
```python
def myfunc():
    global x
    x = 4

myfunc()
print(x)  # Output: 4
```
