# Introduction 

```markdown
# Introduction to Python

## What is Python?
Python is a popular programming language created by **Guido van Rossum** and released in **1991**.

### Applications of Python:
1. Web development (server-side)
2. Software development
3. Mathematics
4. System scripting

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

```markdown
# Python Data Types and String Manipulation

## Python Data Types

### Core Data Types:
- Text Type: `str`
- Numeric Types: `int`, `float`, `complex`
- Sequence Types: `list`, `tuple`, `range`
- Mapping Type: `dict`
- Set Types: `set`, `frozenset`
- Boolean Type: `bool`
- Binary Types: `bytes`, `bytearray`, `memoryview`
- None Type: `NoneType`

---

## Random Number Syntax
To generate a random number within a range:
```python
import random
print(random.randrange(1, 10))
```

---

## Strings

### Multiline Strings:
```python
a = """Lorem ipsum dolor sit amet,
consectetur adipiscing elit,
sed do eiusmod tempor incididunt
ut labore et dolore magna aliqua."""
print(a)
```

### Looping Through a String:
```python
for x in "banana":
    print(x)
```

### String Length:
```python
a = "Hello, World!"
print(len(a))
```

### Check if a Substring is Present:
Use the `in` keyword to check if a substring exists in a string:
```python
txt = "The best things in life are free!"
print("free" in txt)
```

Use it in an `if` statement:
```python
txt = "The best things in life are free!"
if "free" in txt:
    print("Yes, 'free' is present.")
```

### Check if a Substring is NOT Present:
Use the `not in` keyword:
```python
txt = "The best things in life are free!"
print("expensive" not in txt)
```

Use it in an `if` statement:
```python
txt = "The best things in life are free!"
if "expensive" not in txt:
    print("No, 'expensive' is NOT present.")
```

---

## Slicing Strings

### Slice Syntax:
Specify the start and end indices, separated by a colon:
```python
b = "Hello, World!"
print(b[2:5])  # Returns characters at index 2 to 4
```

### Slice from the Start:
```python
b = "Hello, World!"
print(b[:5])  # Returns the first 5 characters
```

### Slice to the End:
```python
b = "Hello, World!"
print(b[2:])  # Returns characters from index 2 to the end
```

---

## Modifying Strings

### Common Methods:
- **Convert to Upper Case**:
```python
a = "Hello, World!"
print(a.upper())
```

- **Convert to Lower Case**:
```python
b = "Hello, World!"
print(b.lower())
```

- **Remove Whitespace**:
```python
c = " Hello, World! "
print(c.strip())  # Removes leading and trailing spaces
```

- **Replace Characters**:
```python
d = "hello world"
print(d.replace("h", "w"))
```

- **Split a String**:
```python
e = "hello, world"
print(e.split(","))  # Splits the string into a list at each comma
```

---

## F-Strings

### Basic F-String Usage:
Add an `f` before the string and use curly braces `{}` for placeholders:
```python
age = 36
txt = f"My name is John, I am {age}"
print(txt)
```

### Placeholders with Modifiers:
Modifiers allow formatting within placeholders. Example:
```python
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt)  # Outputs: The price is 59.00 dollars
```



