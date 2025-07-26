## 16. if / elif / else

The `if`, `elif`, and `else` statements are used to **control the flow** of your program based on conditions.

---

## 🔹 Syntax

```python
if condition1:
    # code block 1
elif condition2:
    # code block 2
else:
    # code block 3
```

* **`if`** checks the first condition
* **`elif`** (short for *else if*) checks additional conditions if `if` is false
* **`else`** runs if none of the above conditions are true

---

## ✅ Basic Example

```python
x = int(input("Enter a number: "))

if x > 0:
    print("Positive number")
elif x < 0:
    print("Negative number")
else:
    print("Zero")
```

---

## 🔹 Multiple `elif`s Allowed

```python
marks = int(input("Enter your score: "))

if marks >= 90:
    print("Grade: A")
elif marks >= 80:
    print("Grade: B")
elif marks >= 70:
    print("Grade: C")
else:
    print("Grade: F")
```

---

## 🔍 Single-Line `if`

```python
age = 20
if age >= 18: print("Adult")
```

---

## 🧠 Boolean Conditions

You can use `and`, `or`, and `not`:

```python
temp = 25

if temp > 20 and temp < 30:
    print("Nice weather")
```

---

## 🚫 Indentation is Mandatory

Each block must be **indented** (usually 4 spaces):

```python
if True:
    print("This is indented correctly")
# Incorrect indentation will cause an error
```
---

## 17. for Loop

A `for` loop in Python is used to **iterate over a sequence** (like a list, string, tuple, or range) and execute a block of code for each item.

---

## 🔹 Basic Syntax

```python
for variable in sequence:
    # code block
```

---

## ✅ Example with `range()`

```python
for i in range(5):
    print(i)
```

**Output:**

```
0
1
2
3
4
```

> `range(5)` generates numbers from `0` to `4` (not including `5`)

---

## 🔹 `range(start, stop, step)`

```python
for i in range(1, 10, 2):
    print(i)
```

**Output:**
`1 3 5 7 9`

---

## 🔹 Looping Through a List

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

---

## 🔹 Looping Through a String

```python
for char in "Python":
    print(char)
```

---

## 🔹 `for` with `else` (Optional)

```python
for i in range(3):
    print(i)
else:
    print("Loop completed")
```

> The `else` block runs **only if the loop finishes without `break`**.

---

## 🔹 Using `break` and `continue`

```python
for i in range(5):
    if i == 3:
        break   # exits the loop
    print(i)

for i in range(5):
    if i == 2:
        continue  # skips this iteration
    print(i)
```
---

## 18. while Loop

A `while` loop is used to **repeat a block of code** **as long as a condition is `True`**.

---

## 🔹 Syntax

```python
while condition:
    # code block
```

* The loop runs **until** the condition becomes **False**.
* You **must** update something inside the loop to avoid an **infinite loop**.

---

## ✅ Basic Example

```python
i = 0
while i < 5:
    print(i)
    i += 1
```

**Output:**

```
0
1
2
3
4
```

---

## 🔹 Infinite Loop (⚠️ Use with caution!)

```python
while True:
    print("This will run forever unless you break it!")
    break  # stops the loop
```

---

## 🔹 `while` with `else`

```python
x = 3
while x > 0:
    print(x)
    x -= 1
else:
    print("Loop ended")
```

---

## 🔹 Using `break` and `continue`

```python
x = 0
while x < 5:
    x += 1
    if x == 3:
        continue  # skips this iteration
    if x == 5:
        break     # exits loop early
    print(x)
```

---

## 🧠 Example: User Input Until Correct

```python
password = ""
while password != "admin123":
    password = input("Enter password: ")

print("Access granted!")
```
---

## 19. break / continue

These are **loop control statements** used to change the normal flow of `for` or `while` loops.

---

## 🔹 `break` Statement

* **Immediately exits** the loop.
* The loop stops even if the condition is still `True`.

### ✅ Example:

```python
for i in range(5):
    if i == 3:
        break
    print(i)
```

**Output:**

```
0
1
2
```

---

## 🔹 `continue` Statement

* **Skips the current iteration** and goes to the **next one**.
* The loop **continues**, but skips the rest of the code **only for that iteration**.

### ✅ Example:

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

**Output:**

```
0
1
3
4
```

---

## 🔄 With `while` Loop

```python
x = 0
while x < 5:
    x += 1
    if x == 3:
        continue
    if x == 5:
        break
    print(x)
```

**Output:**

```
1
2
4
```

---

## 🧠 Use Case: Skip or Exit Based on User Input

```python
while True:
    name = input("Enter your name (or type 'exit'): ")
    if name == "exit":
        break
    if name == "":
        continue
    print("Hello", name)
```
---

## 20. range() Function

The `range()` function is used to generate a **sequence of numbers**, commonly in `for` loops.

---

## 🔹 Syntax

```python
range(stop)
range(start, stop)
range(start, stop, step)
```

| Parameter | Description                                      |
| --------- | ------------------------------------------------ |
| `start`   | (Optional) Starting number (default is `0`)      |
| `stop`    | **(Required)** Ending number (excluded)          |
| `step`    | (Optional) Step between numbers (default is `1`) |

---

## ✅ Examples

### 1. **Basic usage with one argument**

```python
for i in range(5):
    print(i)
```

**Output:**

```
0
1
2
3
4
```

---

### 2. **With start and stop**

```python
for i in range(2, 6):
    print(i)
```

**Output:**

```
2
3
4
5
```

---

### 3. **With step**

```python
for i in range(1, 10, 2):
    print(i)
```

**Output:**

```
1
3
5
7
9
```

---

### 4. **Using negative step (counting backward)**

```python
for i in range(5, 0, -1):
    print(i)
```

**Output:**

```
5
4
3
2
1
```

---

## 🔄 `range()` in Lists

You can convert a `range` to a list:

```python
nums = list(range(1, 6))
print(nums)  # [1, 2, 3, 4, 5]
```

---

## 🛑 Note

* `range()` does **not include** the stop number.
* `step` must **not be 0**, or you'll get an error.

---

## 21. List

A **list** is a built-in data type in Python used to store **a collection of items**.
Lists are **ordered**, **mutable** (can be changed), and can contain **mixed data types**.

---

## 🔹 Creating a List

```python
my_list = [1, 2, 3, 4]
names = ["Alice", "Bob", "Charlie"]
mixed = [1, "two", 3.0, True]
empty = []
```

---

## 🔹 Accessing List Elements (Indexing)

```python
fruits = ["apple", "banana", "cherry"]

print(fruits[0])    # 'apple'
print(fruits[-1])   # 'cherry'
```

---

## 🔹 Slicing a List

```python
print(fruits[0:2])  # ['apple', 'banana']
print(fruits[:])    # ['apple', 'banana', 'cherry']
```

---

## 🔹 Modifying List Elements

```python
fruits[1] = "blueberry"
print(fruits)  # ['apple', 'blueberry', 'cherry']
```

---

## 🔹 List Methods

| Method         | Description                           |
| -------------- | ------------------------------------- |
| `append(x)`    | Adds `x` to the end                   |
| `insert(i, x)` | Inserts `x` at index `i`              |
| `remove(x)`    | Removes first occurrence of `x`       |
| `pop([i])`     | Removes and returns item at index `i` |
| `sort()`       | Sorts the list in ascending order     |
| `reverse()`    | Reverses the list                     |
| `clear()`      | Removes all items                     |
| `index(x)`     | Returns index of first `x`            |
| `count(x)`     | Counts how many times `x` appears     |

---

### ✅ Example: Common Operations

```python
numbers = [3, 1, 4, 1, 5]

numbers.append(9)         # [3, 1, 4, 1, 5, 9]
numbers.insert(1, 10)     # [3, 10, 1, 4, 1, 5, 9]
numbers.remove(1)         # [3, 10, 4, 1, 5, 9] (removes first 1)
numbers.sort()            # [1, 3, 4, 5, 9, 10]
numbers.reverse()         # [10, 9, 5, 4, 3, 1]
```

---

## 🔄 Looping Through a List

```python
for fruit in fruits:
    print(fruit)
```

---

## 🔎 Check Membership

```python
if "apple" in fruits:
    print("Apple is in the list")
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
