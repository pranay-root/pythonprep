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

---

## Python Lists

### Python Built-in Data Types:
1. **Lists**  
2. Tuple  
3. Set  
4. Dictionary  

---

### Lists:
- Created using square brackets:  
  ```python
  mylist = ["apple", "banana", "cherry"]
  print(mylist)
  ```
- **Characteristics**:
  - Ordered.
  - Changeable.
  - Allow duplicate values.
  - Indexed (starting at 0).

---

### Properties of Lists:
#### Ordered Lists:
- Items have a defined order that does not change.
- New items are added to the end.

#### Changeable Lists:
- You can modify, add, and remove items after creation.

---

### Syntax and Examples:

#### Changing Items in a List:
1. **Change Item Value**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   mylist[1] = "blackcurrant"
   print(mylist)
   ```

2. **Change a Range of Values**:
   ```python
   mylist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
   mylist[1:3] = ["blackcurrant", "watermelon"]
   print(mylist)
   ```

#### Adding Items to a List:
1. **Insert a New Item**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   mylist.insert(2, "watermelon")
   print(mylist)
   ```

2. **Append an Item**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   mylist.append("orange")
   print(mylist)
   ```

3. **Extend a List**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   tropical = ["mango", "pineapple", "papaya"]
   mylist.extend(tropical)
   print(mylist)
   ```

---

### Removing Items from a List:
1. **Remove a Specified Item**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   mylist.remove("banana")
   print(mylist)
   ```

2. **Remove a Specified Index**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   mylist.pop(1)
   print(mylist)
   ```

3. **Delete an Index**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   del mylist[0]
   print(mylist)
   ```

4. **Clear the Entire List**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   mylist.clear()
   print(mylist)
   ```

---

### Looping Through a List:
1. **Loop Through Items**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   for x in mylist:
       print(x)
   ```

2. **Loop Through Indexes**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   for i in range(len(mylist)):
       print(mylist[i])
   ```

3. **Using a While Loop**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   i = 0
   while i < len(mylist):
       print(mylist[i])
       i += 1
   ```

4. **Using List Comprehension**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   [print(x) for x in mylist]
   ```

---

### List Comprehension:
- Shorter syntax to create lists:
  ```python
  newlist = [expression for item in iterable if condition]
  ```

**Example**:
```python
fruits = ["apple", "banana", "cherry"]
newlist = [fruit.upper() for fruit in fruits if "a" in fruit]
print(newlist)
```

---

### Sorting Lists:
1. **Alphanumeric Sorting**:
   ```python
   mylist = ["orange", "mango", "kiwi", "pineapple", "banana"]
   mylist.sort()
   print(mylist)
   ```

2. **Descending Order**:
   ```python
   mylist = ["orange", "mango", "kiwi", "pineapple", "banana"]
   mylist.sort(reverse=True)
   print(mylist)
   ```

3. **Custom Sort**:
   ```python
   def myfunc(n):
       return abs(n - 50)

   mylist = [100, 50, 65, 82, 23]
   mylist.sort(key=myfunc)
   print(mylist)
   ```

4. **Reverse the List**:
   ```python
   mylist = ["banana", "Orange", "Kiwi", "cherry"]
   mylist.reverse()
   print(mylist)
   ```

---

### Copying a List:
1. **Using `copy()`**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   newlist = mylist.copy()
   print(newlist)
   ```

2. **Using Slice Operator**:
   ```python
   mylist = ["apple", "banana", "cherry"]
   newlist = mylist[:]
   print(newlist)
   ```

---

### Joining Lists:
1. **Concatenation**:
   ```python
   list1 = ["a", "b", "c"]
   list2 = [1, 2, 3]
   combined_list = list1 + list2
   print(combined_list)
   ```

2. **Using `extend()`**:
   ```python
   list1 = ["a", "b", "c"]
   list2 = [1, 2, 3]
   list1.extend(list2)
   print(list1)
   ```

--- 

### **Python Tuples**

A tuple is a collection which is ordered and **unchangeable**.

Example:
```python
thistuple = ("apple", "banana", "cherry")
print(thistuple)
```

- **Tuple characteristics**:
  - **Ordered**: The items have a defined order, and that order will not change.
  - **Unchangeable**: Once a tuple is created, you cannot modify it.
  - **Allows duplicate values**: Tuples can contain duplicate values.

---

### **Changing Tuple Values**

Although tuples are unchangeable, you can change their items by converting them to a list, modifying the list, and converting it back to a tuple.

**Example**:
```python
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)
print(x)
```

---

### **Adding Items to a Tuple**

You cannot directly add items to a tuple, but you can convert it to a list, add items, and then convert it back to a tuple.

**Example**:
```python
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.append("orange")
thistuple = tuple(y)
```

---

### **Add Tuple to a Tuple**

You can concatenate two tuples using `+=`.

**Example**:
```python
thistuple = ("apple", "banana", "cherry")
y = ("orange",)
thistuple += y
print(thistuple)
```

---

### **Removing Items from a Tuple**

To remove an item, convert the tuple to a list, remove the item, and then convert it back to a tuple.

**Example**:
```python
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.remove("apple")
thistuple = tuple(y)
```

---

### **Unpacking a Tuple**

You can unpack the values of a tuple into separate variables.

**Example**:
```python
fruits = ("apple", "banana", "cherry")
(green, yellow, red) = fruits
print(green)
print(yellow)
print(red)
```

---

### **Using Asterisk (*) for Unpacking**

You can use an asterisk (`*`) to capture multiple items into one variable.

**Example**:
```python
list = ("cat", "dog", "hacker", "hunt")
(1, 2, *3) = list
print(1, 3)
print(2)
```

---

### **Join Two Tuples**

You can join two tuples using the `+` operator.

**Example**:
```python
tuple1 = ("a", "b", "c")
tuple2 = (1, 2, 3)
tuple3 = tuple1 + tuple2
print(tuple3)
```

---

### **Tuple Methods**

1. **`count()`**: Returns the number of times a specified value occurs in a tuple.
   ```python
   thistuple = ("apple", "banana", "cherry", "apple")
   print(thistuple.count("apple"))  # Output: 2
   ```

2. **`index()`**: Searches the tuple for a specified value and returns the position of where it was found.
   ```python
   thistuple = ("apple", "banana", "cherry")
   print(thistuple.index("banana"))  # Output: 1
   ```

---

### **Python Sets**

A **set** is a collection used to store multiple items in a single variable. It is unordered, unchangeable*, and unindexed.

Sets are written with curly brackets.

**Example**:
```python
thisset = {"apple", "banana", "cherry"}
print(thisset)
```

- **Set Characteristics**:
  - **Unordered**: Items in a set do not have a defined order.
  - **Unchangeable**: Once a set is created, its items cannot be changed.
  - **No Duplicates**: Duplicates are not allowed in sets. Duplicate items are ignored.

---

### **set() Constructor**

You can also create a set using the `set()` constructor.

**Example**:
```python
thisset = set(("apple", "banana", "cherry"))  # Note the double round-brackets
print(thisset)
```

---

### **Access Set Items**

You cannot access set items by index or key. However, you can loop through the set using a for loop or use the `in` keyword to check if a value is present in the set.

**Examples**:
```python
thisset = {"apple", "banana", "cherry"}
for x in thisset:
    print(x)

thisset = {"apple", "banana", "cherry"}
print("banana" in thisset)  # True

thisset = {"apple", "banana", "cherry"}
print("banana" not in thisset)  # False
```

---

### **Add Items**

To add an item to a set, use the `add()` method.

**Example**:
```python
thisset = {"apple", "banana", "cherry"}
thisset.add("orange")
print(thisset)
```

You can add items from another set into the current set using the `update()` method.

**Example**:
```python
x = {"hello", "one"}
y = {"yes", "abc"}
x.update(y)
print(x)
```

---

### **Remove Items**

You can remove items using `remove()` or `discard()` methods.

**Examples**:
```python
thisset = {"apple", "banana", "cherry"}
thisset.remove("banana")
print(thisset)

thisset = {"apple", "banana", "cherry"}
thisset.discard("banana")
print(thisset)
```

---

### **Join Sets**

There are multiple ways to join two or more sets in Python:
- **`union()`** and **`update()`** methods join all items from both sets.
- **`intersection()`** keeps only the duplicates.
- **`difference()`** keeps items from the first set that are not in the other set(s).
- **`symmetric_difference()`** keeps items that are not common to both sets.

---

### **Union()**

The `union()` method joins two sets.

**Examples**:
```python
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}
set3 = set1.union(set2)
print(set3)

# Alternatively, you can use the `|` operator
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}
set3 = set1 | set2
print(set3)
```

---

### **Join Multiple Sets**

You can join multiple sets using `union()`.

**Example**:
```python
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}
set3 = {"John", "Elena"}
set4 = {"apple", "bananas", "cherry"}
myset = set1.union(set2, set3, set4)
print(myset)
```

---

### **Update()**

The `update()` method inserts the items in another set into the current set.

**Example**:
```python
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}
set1.update(set2)
print(set1)
```

---

### **Intersection()**

The `intersection()` method keeps only the duplicates (common items).

**Examples**:
```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1.intersection(set2)
print(set3)

# Alternatively, you can use the `&` operator
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1 & set2
print(set3)
```

---

### **intersection_update()**

The `intersection_update()` method keeps only the duplicates and modifies the original set.

**Example**:
```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set1.intersection_update(set2)
print(set1)
```

---

### **Difference()**

The `difference()` method returns a new set with items from the first set that are not in the other set(s).

**Examples**:
```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1.difference(set2)
print(set3)

# Alternatively, you can use the `-` operator
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1 - set2
print(set3)
```

---

### **difference_update()**

The `difference_update()` method removes items from the original set that are also in the other set(s).

**Example**:
```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set1.difference_update(set2)
print(set1)
```

---

### **symmetric_difference()**

The `symmetric_difference()` method keeps only the elements that are not present in both sets.

**Examples**:
```python
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1.symmetric_difference(set2)
print(set3)

# Alternatively, you can use the `^` operator
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set3 = set1 ^ set2
print(set3)

# Modify the original set with `symmetric_difference_update()`
set1 = {"apple", "banana", "cherry"}
set2 = {"google", "microsoft", "apple"}
set1.symmetric_difference_update(set2)
print(set1)
```

---


