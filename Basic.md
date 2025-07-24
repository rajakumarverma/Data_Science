# 🐍 Python Basics Concepts

## 1. Variable Assignment

In Python, **variables** are used to store data. **Variable assignment** means assigning a value to a variable name so it can be used later in your code.

###  Basic Syntax

```python
variable_name = value
```

* `=` is the **assignment operator**
* `variable_name` is the name you choose
* `value` is the data you're assigning

**Example:**

```python
x = 10
name = "Alice"
is_active = True
```

## 2. Variable Naming Rules

* Must start with a letter (a–z, A–Z) or underscore (`_`)
* Cannot start with a number
* Can contain letters, numbers, and underscores
* Cannot be a Python keyword (`if`, `for`, `while`, etc.)

**Valid:**

```python
age = 25
_user_name = "bob"
score2 = 87
```

**Invalid:**

```python
2cool = "nope"    # starts with a number
for = "loop"      # "for" is a keyword
```

###  Multiple Assignments

Python allows multiple assignments in one line:

```python
a, b, c = 1, 2, 3
```

All assigned to the same value:

```python
x = y = z = 0
```

###  Swapping Variables

Python lets you swap variables without a temporary variable:

```python
a = 5
b = 10
a, b = b, a
```

###  Dynamic Typing

Python is dynamically typed, so you don't declare types explicitly:

```python
x = 10       # x is an int
x = "Hello"  # now x is a str
```

```python
x = 10
name = "Alice"
# (No output, stores values)
```

---

## 2. Variable Naming Rules

- Start with letter or `_`
- Use letters, numbers, and `_`
- Case-sensitive, no keywords

---

## 3. Data Types

`int`, `float`, `str`, `bool`, `list`, `tuple`, `dict`, `set`, `None`

---

## 4. Type Checking

```python
type(x)           # <class 'int'>
isinstance(x, int) # True
```

---

## 5. Type Casting

```python
int("5")         # 5
float("3.14")    # 3.14
str(10)          # '10'
```

---

## 6. Input from User

```python
name = input("Enter name: ")  # User types: Bob
print(name)                   # Bob
```

---

## 7. Output Print

```python
print("Hello", name)   # Hello Bob
print(f"Hi, {name}")   # Hi, Bob
```

---

## 8. String Indexing

```python
s = "Python"
print(s[0], s[-1])     # P n
```

---

## 9. String Slicing

```python
print(s[1:4])          # yth
print(s[:3])           # Pyt
print(s[3:])           # hon
```

---

## 10. String Methods

```python
"hello".upper()         # HELLO
"HELLO".lower()         # hello
"abc".replace("a", "z") # zbc
```

---

## 11. Arithmetic Operators

```python
7 + 3     # 10
7 / 3     # 2.3333
7 // 3    # 2
7 % 3     # 1
2 ** 3    # 8
```

---

## 12. Comparison Operators

```python
5 == 5    # True
5 != 3    # True
3 > 2     # True
3 <= 3    # True
```

---

## 13. Logical Operators

```python
True and False   # False
True or False    # True
not True         # False
```

---

## 14. Membership Operators

```python
'a' in "apple"       # True
3 not in [1, 2, 4]   # True
```

---

## 15. Identity Operators

```python
a = [1, 2]
b = a
a is b              # True
a is not [1, 2]     # True
```

---

## 16. if / elif / else

```python
x = 5
if x > 0:
    print("Positive")     # Positive
elif x == 0:
    print("Zero")
else:
    print("Negative")
```

---

## 17. for Loop

```python
for i in range(3):
    print(i)
# Output:
# 0
# 1
# 2
```

---

## 18. while Loop

```python
i = 0
while i < 3:
    print(i)
    i += 1
# Output:
# 0
# 1
# 2
```

---

## 19. break / continue

```python
for i in range(5):
    if i == 3:
        break
    if i == 1:
        continue
    print(i)
# Output:
# 0
# 2
```

---

## 20. range() Function

```python
list(range(5))        # [0, 1, 2, 3, 4]
list(range(1, 5))     # [1, 2, 3, 4]
list(range(0, 10, 2)) # [0, 2, 4, 6, 8]
```

---

## 21. List

```python
fruits = ["apple", "banana"]
print(fruits)          # ['apple', 'banana']
```

---

## 22. List Indexing

```python
fruits[0]              # 'apple'
fruits[-1]             # 'banana'
```

---

## 23. List Slicing

```python
fruits[0:1]            # ['apple']
fruits[1:]             # ['banana']
```

---

## 24. List Methods

```python
fruits.append("orange")
print(fruits)          # ['apple', 'banana', 'orange']

fruits.remove("banana")
print(fruits)          # ['apple', 'orange']
```

---

## 25. Tuple

```python
colors = ("red", "green")
print(colors[0])       # 'red'
```

---

## 26. Set

```python
nums = {1, 2, 2, 3}
print(nums)            # {1, 2, 3}
```

---

## 27. Dictionary

```python
person = {"name": "Alice", "age": 30}
print(person["name"])  # Alice
```

---

## 28. Function

```python
def greet(name):
    print(f"Hello, {name}")

greet("Bob")           # Hello, Bob
```

---

## 29. *args and **kwargs

```python
def example(*args, **kwargs):
    print(args)
    print(kwargs)

example(1, 2, name="Alice")
# Output:
# (1, 2)
# {'name': 'Alice'}
```

---

## 30. return Statement

```python
def square(x):
    return x * x

print(square(4))       # 16
```
---

### 31. File Reading (`r`)

Open a file to read its content.

```python
with open('file.txt', 'r') as file:
    content = file.read()
print(content)
```

---

### 32. File Writing (`w`)

Open a file to write data (overwrites existing).

```python
with open('file.txt', 'w') as file:
    file.write("Hello World")
```

---

### 33. Append to File (`a`)

Open a file to add data at the end.

```python
with open('file.txt', 'a') as file:
    file.write("\nNew line")
```

---

### 34. Try/Except

Handle errors gracefully to avoid crashes.

```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

---

### 35. Finally Clause

Code that runs no matter what (after try/except).

```python
try:
    f = open('file.txt')
finally:
    f.close()
```

---

### 36. Raise Exception

Manually trigger an error.

```python
def check_age(age):
    if age < 18:
        raise ValueError("Too young!")
check_age(15)  # Raises ValueError
```

---

### 37. Class & Object

Create your own data types (blueprints).

```python
class Person:
    def __init__(self, name):
        self.name = name

p = Person("Alice")
print(p.name)  # Alice
```

---

### 38. Class Methods

Methods that act on the class, not instance.

```python
class Person:
    count = 0

    @classmethod
    def increment(cls):
        cls.count += 1

Person.increment()
print(Person.count)  # 1
```

---

### 39. Inheritance

Create a new class based on an existing one.

```python
class Animal:
    def speak(self):
        print("Animal sound")

class Dog(Animal):
    def speak(self):
        print("Woof")

d = Dog()
d.speak()  # Woof
```

---

### 40. `super()`

Call parent class methods inside child classes.

```python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)
        self.breed = breed
```

---

### 41. `__str__()` Method

Defines how object prints as a string.

```python
class Person:
    def __init__(self, name):
        self.name = name
    def __str__(self):
        return f"Person: {self.name}"

p = Person("Alice")
print(p)  # Person: Alice
```

---

### 42. Importing Modules

Use code from other files/libraries.

```python
import math
print(math.sqrt(16))  # 4.0
```

---

### 43. `from ... import`

Import specific parts of a module.

```python
from math import pi
print(pi)  # 3.14159...
```

---

### 44. Creating Modules

Save functions/classes in `.py` files and import them.

```python
# mymodule.py
def greet():
    print("Hello")

# another_file.py
import mymodule
mymodule.greet()  # Hello
```

---

### 45. pip / Package Install

Install third-party packages.

```bash
pip install requests
```

---

### 46. Lambda Function

Anonymous, one-line functions.

```python
square = lambda x: x * x
print(square(5))  # 25
```

---

### 47. Map Function

Apply a function to all items in a list.

```python
nums = [1, 2, 3]
squares = list(map(lambda x: x**2, nums))
print(squares)  # [1, 4, 9]
```

---

### 48. Filter Function

Filter items by a condition.

```python
nums = [1, 2, 3, 4]
evens = list(filter(lambda x: x % 2 == 0, nums))
print(evens)  # [2, 4]
```

---

### 49. Reduce Function

Apply a rolling computation to a list.

```python
from functools import reduce
nums = [1, 2, 3, 4]
total = reduce(lambda x, y: x + y, nums)
print(total)  # 10
```

---

### 50. List Comprehension

Create lists easily and readably.

```python
squares = [x**2 for x in range(5)]
print(squares)  # [0, 1, 4, 9, 16]
```

---

### 51. Dictionary Comprehension

Create dictionaries in one line.

```python
squares = {x: x**2 for x in range(5)}
print(squares)  # {0:0,1:1,2:4,3:9,4:16}
```

---

### 52. Generator Function

Generate items one by one, saving memory.

```python
def count_up_to(n):
    count = 1
    while count <= n:
        yield count
        count += 1

for num in count_up_to(3):
    print(num)
# 1
# 2
# 3
```

---

### 53. Iterators

Objects you can loop over.

```python
nums = [1, 2, 3]
it = iter(nums)
print(next(it))  # 1
print(next(it))  # 2
```

---

### 54. Decorators

Modify functions without changing them.

```python
def decorator(func):
    def wrapper():
        print("Before")
        func()
        print("After")
    return wrapper

@decorator
def say_hello():
    print("Hello")

say_hello()
# Before
# Hello
# After
```

---

### 55. Regular Expressions

Pattern matching in strings (import `re`).

```python
import re
pattern = r'\d+'
result = re.findall(pattern, 'There are 12 apples and 34 oranges')
print(result)  # ['12', '34']
```

---

### 56. JSON Parsing

Work with JSON data.

```python
import json
data = '{"name": "Alice", "age": 30}'
parsed = json.loads(data)
print(parsed['name'])  # Alice
```

---

### 57. Date & Time

Work with dates and times.

```python
from datetime import datetime
now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M:%S"))
```

---

### 58. Math / Random Lib

Useful math functions and random numbers.

```python
import math, random
print(math.pi)          # 3.141592653589793
print(random.randint(1, 10))  # random number 1-10
```

---

### 59. SQLite DB Access

Basic database interaction.

```python
import sqlite3
conn = sqlite3.connect(':memory:')
c = conn.cursor()
c.execute('CREATE TABLE test(id INTEGER)')
conn.close()
```

---

### 60. Virtual Env

Isolate project dependencies (run in terminal).

```bash
python -m venv env
source env/bin/activate  # Linux/Mac
env\Scripts\activate     # Windows
```

---

### 61. Web Scraping

Extract data from websites.

```python
import requests
from bs4 import BeautifulSoup

r = requests.get('https://example.com')
soup = BeautifulSoup(r.text, 'html.parser')
print(soup.title.text)
```

---

### 62. Pandas (Basic)

Powerful data analysis tool.

```python
import pandas as pd
df = pd.DataFrame({'A':[1,2], 'B':[3,4]})
print(df)
```

---

### 63. NumPy (Basic)

Efficient numerical computing.

```python
import numpy as np
arr = np.array([1, 2, 3])
print(arr * 2)  # [2 4 6]
```

---

### 64. Docstrings

Documentation inside functions/classes.

```python
def greet():
    """Prints a greeting message."""
    print("Hello")

print(greet.__doc__)  # Prints docstring
```

---

### 65. `__name__ == "__main__"`

Run code only if script is executed directly.

```python
def main():
    print("Run directly")

if __name__ == "__main__":
    main()
```
