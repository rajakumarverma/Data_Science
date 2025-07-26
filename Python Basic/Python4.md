### 45. Generator Function

A **generator function** is a special type of function that **yields values one at a time**, using the `yield` keyword instead of `return`.

It **remembers its state** between calls, which makes it **memory-efficient** when working with large data or infinite sequences.

---

## 🔹 Syntax

```python
def my_generator():
    yield value1
    yield value2
    ...
```

---

## ✅ Example 1: Simple Generator

```python
def count_up_to(n):
    count = 1
    while count <= n:
        yield count
        count += 1

gen = count_up_to(3)

for num in gen:
    print(num)
```

**Output:**

```
1
2
3
```

---

## ✅ Example 2: Use `next()`

```python
def numbers():
    yield 10
    yield 20

g = numbers()
print(next(g))  # 10
print(next(g))  # 20
```

---

## ✅ Example 3: Generator Expression (like list comprehension)

```python
squares = (x**2 for x in range(5))

for s in squares:
    print(s)
```

---

## ✅ Why Use Generators?

| Feature          | Benefit                                |
| ---------------- | -------------------------------------- |
| `yield`          | Pauses function and saves state        |
| Memory-efficient | Does **not** store full list in memory |
| Lazy evaluation  | Values produced **on demand**          |
| Useful for       | Large files, streams, pipelines        |

---

## ✅ Real-World Example: Reading a File Line by Line

```python
def read_file_line_by_line(filename):
    with open(filename, 'r') as f:
        for line in f:
            yield line.strip()

for line in read_file_line_by_line('data.txt'):
    print(line)
```

---

## 🧠 Summary

* Use `yield` instead of `return` to create a generator
* Maintains state between iterations
* More efficient than returning a full list in some cases

---

### 46. Iterators

An **iterator** is any object in Python that **can be iterated (looped) over**, one element at a time.
It uses two main methods:

* `__iter__()` → returns the iterator object itself
* `__next__()` → returns the **next value** from the iterator

---

## ✅ What is Iterable vs Iterator?

| Term         | Description                               | Examples                                  |
| ------------ | ----------------------------------------- | ----------------------------------------- |
| **Iterable** | An object you can loop over               | `list`, `tuple`, `str`, `set`, etc.       |
| **Iterator** | An object that **remembers its position** | Result of calling `iter()` on an iterable |

---

## 🔹 Example: Creating an Iterator

```python
nums = [1, 2, 3]
it = iter(nums)

print(next(it))  # 1
print(next(it))  # 2
print(next(it))  # 3
```

---

## 🔹 Looping with an Iterator

```python
nums = [10, 20, 30]
it = iter(nums)

for num in it:
    print(num)
```

---

## 🔹 Custom Iterator Class

```python
class Counter:
    def __init__(self, max):
        self.max = max
        self.current = 1

    def __iter__(self):
        return self

    def __next__(self):
        if self.current <= self.max:
            val = self.current
            self.current += 1
            return val
        else:
            raise StopIteration

c = Counter(3)
for num in c:
    print(num)
```

**Output:**

```
1
2
3
```

---

## 🔹 Summary

| Concept          | Explanation                          |
| ---------------- | ------------------------------------ |
| `iter(obj)`      | Gets iterator from iterable          |
| `next(iterator)` | Gets next item                       |
| `StopIteration`  | Raised when there are no more items  |
| Custom Iterator  | Define `__iter__()` and `__next__()` |

---

### 47. Decorators

A **decorator** is a **function that modifies another function**, adding extra behavior **before or after** the original function runs — without changing its code.

It's often used for:

* Logging
* Authentication
* Timing
* Access control
* Caching

---

## 🔹 Basic Syntax

```python
def decorator_function(original_function):
    def wrapper():
        print("Before the function runs")
        original_function()
        print("After the function runs")
    return wrapper
```

Then apply it:

```python
@decorator_function
def say_hello():
    print("Hello!")

say_hello()
```

---

## ✅ Output:

```
Before the function runs
Hello!
After the function runs
```

---

## 🔹 Example with `*args` and `**kwargs`

```python
def debug(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with {args} {kwargs}")
        return func(*args, **kwargs)
    return wrapper

@debug
def add(a, b):
    return a + b

print(add(3, 4))  # Output: Calling add with (3, 4) {}
                 #         7
```

---

## ✅ Multiple Decorators

```python
def bold(func):
    def wrapper():
        return "<b>" + func() + "</b>"
    return wrapper

def italic(func):
    def wrapper():
        return "<i>" + func() + "</i>"
    return wrapper

@bold
@italic
def greet():
    return "Hello"

print(greet())  # <b><i>Hello</i></b>
```

---

## ✅ Built-in Decorators Example

* `@staticmethod`
* `@classmethod`
* `@property`

---

## 🧠 Summary

| Feature           | Description                                |
| ----------------- | ------------------------------------------ |
| `@decorator`      | Short-hand to wrap a function              |
| `*args, **kwargs` | Allow decorators to work with any function |
| Reusable          | Keeps code DRY and modular                 |

---

### 48. Regular Expressions

**Regular Expressions (RegEx)** are patterns used to **match, search, or manipulate text**.
Python provides the `re` module to work with regex.

---

## 🔹 Import the `re` Module

```python
import re
```

---

## 🔹 Common Functions

| Function       | Description                                     |
| -------------- | ----------------------------------------------- |
| `re.match()`   | Checks for a match **at the start** of a string |
| `re.search()`  | Searches for **first match** anywhere           |
| `re.findall()` | Returns **all matches** as a list               |
| `re.sub()`     | Replaces matched text                           |

---

## ✅ Basic Patterns

| Pattern  | Matches                            |
| -------- | ---------------------------------- |
| `.`      | Any character except newline       |
| `\d`     | Digit (0–9)                        |
| `\D`     | Non-digit                          |
| `\w`     | Word character (a-z, A-Z, 0–9, \_) |
| `\W`     | Non-word character                 |
| `\s`     | Whitespace                         |
| `\S`     | Non-whitespace                     |
| `^`      | Start of string                    |
| `$`      | End of string                      |
| `[...]`  | Any character in set               |
| `[^...]` | Any character **not** in set       |
| `*`      | 0 or more repetitions              |
| `+`      | 1 or more repetitions              |
| `{n}`    | Exactly n repetitions              |
| `{n,m}`  | Between n and m repetitions        |

---

## ✅ Example 1: Validate Email

```python
import re

email = "user@example.com"
pattern = r'^[\w\.-]+@[\w\.-]+\.\w+$'

if re.match(pattern, email):
    print("Valid email")
else:
    print("Invalid email")
```

---

## ✅ Example 2: Extract All Numbers

```python
text = "My phone number is 123-456-7890 and zip is 90210"
numbers = re.findall(r'\d+', text)
print(numbers)  # ['123', '456', '7890', '90210']
```

---

## ✅ Example 3: Replace Words

```python
text = "I love cats"
new_text = re.sub(r'cats', 'dogs', text)
print(new_text)  # I love dogs
```

---

## 🧠 Tip: Use Raw Strings (`r""`)

Always write patterns as **raw strings** to avoid escaping backslashes:

```python
pattern = r'\d+'  # NOT '\\d+'
```

---

## 🧰 Summary

| Tool           | Use Case                      |
| -------------- | ----------------------------- |
| `re.match()`   | Match from the beginning      |
| `re.search()`  | Search anywhere in the string |
| `re.findall()` | Find all matching substrings  |
| `re.sub()`     | Replace matched substrings    |

---

### 49. JSON Parsing

**JSON (JavaScript Object Notation)** is a common format for **data exchange** (e.g., APIs, config files).
Python’s built-in `json` module lets you **parse** JSON into Python objects and **convert** Python objects to JSON.

---

## 🔹 Step 1: Import the `json` Module

```python
import json
```

---

## ✅ Parsing JSON → Python (`json.loads()`)

```python
import json

json_data = '{"name": "Alice", "age": 25, "city": "New York"}'
python_dict = json.loads(json_data)

print(python_dict)
print(python_dict['name'])  # Output: Alice
```

> 🔸 `json.loads()` converts a **JSON string** to a **Python dictionary**.

---

## ✅ Converting Python → JSON (`json.dumps()`)

```python
data = {"name": "Bob", "age": 30, "active": True}
json_string = json.dumps(data)

print(json_string)
```

> 🔸 `json.dumps()` converts a **Python object** to a **JSON string**.

---

## ✅ Reading JSON from a File (`json.load()`)

```python
with open('data.json', 'r') as file:
    data = json.load(file)

print(data)
```

> 🔸 `json.load()` reads and parses JSON **from a file**.

---

## ✅ Writing JSON to a File (`json.dump()`)

```python
info = {"product": "Laptop", "price": 799}

with open('output.json', 'w') as file:
    json.dump(info, file)
```

> 🔸 `json.dump()` writes JSON **to a file**.

---

## 🔹 Common Python ↔ JSON Type Mapping

| Python           | JSON         |
| ---------------- | ------------ |
| `dict`           | object       |
| `list`           | array        |
| `str`            | string       |
| `int`, `float`   | number       |
| `True` / `False` | true / false |
| `None`           | null         |

---

## 🧠 Extra: Pretty Print JSON

```python
print(json.dumps(data, indent=4))
```
---

### 50. Date & Time

Python’s built-in `datetime` module makes it easy to **work with dates and times** — getting the current time, formatting dates, doing arithmetic, and more.

---

## 🔹 Import the Module

```python
import datetime
```

---

## ✅ Get Current Date and Time

```python
from datetime import datetime

now = datetime.now()
print("Now:", now)
print("Date:", now.date())
print("Time:", now.time())
```

---

## ✅ Format Dates (`strftime()`)

```python
from datetime import datetime

now = datetime.now()
formatted = now.strftime("%Y-%m-%d %H:%M:%S")
print(formatted)  # e.g. 2025-07-26 14:30:45
```

### 📌 Common Format Codes:

| Code | Meaning         | Example |
| ---- | --------------- | ------- |
| `%Y` | Year (4 digits) | 2025    |
| `%m` | Month (01–12)   | 07      |
| `%d` | Day (01–31)     | 26      |
| `%H` | Hour (00–23)    | 14      |
| `%M` | Minute (00–59)  | 30      |
| `%S` | Second (00–59)  | 45      |

---

## ✅ Parse String to Date (`strptime()`)

```python
from datetime import datetime

date_str = "2025-07-26"
date_obj = datetime.strptime(date_str, "%Y-%m-%d")
print(date_obj)  # 2025-07-26 00:00:00
```

---

## ✅ Get Today's Date

```python
from datetime import date

today = date.today()
print(today)
```

---

## ✅ Date Arithmetic

```python
from datetime import timedelta, date

today = date.today()
future = today + timedelta(days=10)
past = today - timedelta(days=5)

print("10 days from now:", future)
print("5 days ago:", past)
```

---

## ✅ Get Individual Components

```python
now = datetime.now()

print(now.year)   # 2025
print(now.month)  # 7
print(now.day)    # 26
```

---

## 🧠 Summary

| Task              | Tool             |
| ----------------- | ---------------- |
| Current date/time | `datetime.now()` |
| Format date/time  | `strftime()`     |
| Parse from string | `strptime()`     |
| Add/Subtract days | `timedelta()`    |
| Just date         | `date.today()`   |

---

### 51. Math / Random Lib

Python provides built-in libraries to handle **mathematical operations** and **randomization**:

---

## 📐 `math` Module (Mathematical Functions)

### ✅ Importing:

```python
import math
```

### 🔹 Common `math` Functions:

| Function            | Description                  | Example                     |
| ------------------- | ---------------------------- | --------------------------- |
| `math.sqrt(x)`      | Square root                  | `math.sqrt(16)` → `4.0`     |
| `math.pow(x, y)`    | Power (x^y)                  | `math.pow(2, 3)` → `8.0`    |
| `math.factorial(n)` | Factorial                    | `math.factorial(5)` → `120` |
| `math.floor(x)`     | Round **down**               | `math.floor(3.9)` → `3`     |
| `math.ceil(x)`      | Round **up**                 | `math.ceil(3.1)` → `4`      |
| `math.pi`           | π (3.14159...)               | `math.pi`                   |
| `math.e`            | Euler’s number (2.718...)    | `math.e`                    |
| `math.log(x, base)` | Logarithm (default base `e`) | `math.log(100, 10)` → `2`   |

---

## 🎲 `random` Module (Randomization)

### ✅ Importing:

```python
import random
```

### 🔹 Common `random` Functions:

| Function                | Description                        | Example                        |
| ----------------------- | ---------------------------------- | ------------------------------ |
| `random.random()`       | Random float between 0 and 1       | `0.7481...`                    |
| `random.randint(a, b)`  | Random int in range \[a, b]        | `random.randint(1, 6)`         |
| `random.choice(seq)`    | Random item from list/tuple/string | `random.choice(['a','b','c'])` |
| `random.shuffle(list)`  | Shuffle the list in-place          |                                |
| `random.uniform(a, b)`  | Random float between a and b       | `random.uniform(1, 5)`         |
| `random.sample(pop, k)` | Get `k` unique random elements     | `random.sample(range(10), 3)`  |

---

## ✅ Examples

### 1. Roll a Dice

```python
import random
print(random.randint(1, 6))
```

### 2. Shuffle a List

```python
items = [1, 2, 3, 4, 5]
random.shuffle(items)
print(items)
```

### 3. Calculate Circle Area

```python
import math
radius = 5
area = math.pi * math.pow(radius, 2)
print(area)
```

---

## 🧠 Summary

| Library  | Use For                          |
| -------- | -------------------------------- |
| `math`   | Advanced mathematical operations |
| `random` | Simulations, games, sampling     |

---

### 52. SQLite DB Access

SQLite is a **lightweight, built-in SQL database** in Python — perfect for small projects or prototyping.

Python provides the `sqlite3` module to **connect**, **create tables**, **insert data**, and **run queries**.

---

## 🔹 Step 1: Import & Connect

```python
import sqlite3

# Connect to a database (creates if not exists)
conn = sqlite3.connect('example.db')

# Create a cursor object to execute SQL
cursor = conn.cursor()
```

---

## 🔹 Step 2: Create a Table

```python
cursor.execute('''
CREATE TABLE IF NOT EXISTS users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT,
    age INTEGER
)
''')
```

---

## 🔹 Step 3: Insert Data

```python
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Alice", 30))
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Bob", 25))
conn.commit()  # Save changes
```

> ✅ Always use `?` placeholders to prevent SQL injection.

---

## 🔹 Step 4: Read Data

```python
cursor.execute("SELECT * FROM users")
rows = cursor.fetchall()

for row in rows:
    print(row)
```

---

## 🔹 Step 5: Update & Delete

```python
# Update
cursor.execute("UPDATE users SET age = ? WHERE name = ?", (31, "Alice"))

# Delete
cursor.execute("DELETE FROM users WHERE name = ?", ("Bob",))

conn.commit()
```

---

## 🔹 Step 6: Close Connection

```python
conn.close()
```

---

## ✅ Example Summary

```python
import sqlite3

conn = sqlite3.connect('people.db')
cursor = conn.cursor()

cursor.execute('''CREATE TABLE IF NOT EXISTS people (id INTEGER PRIMARY KEY, name TEXT, age INTEGER)''')
cursor.execute("INSERT INTO people (name, age) VALUES (?, ?)", ("Charlie", 22))
conn.commit()

cursor.execute("SELECT * FROM people")
print(cursor.fetchall())

conn.close()
```

---

## 🔹 Optional: Convert Rows to Dictionaries

```python
conn.row_factory = sqlite3.Row
cursor = conn.cursor()

cursor.execute("SELECT * FROM users")
row = cursor.fetchone()
print(dict(row))  # {'id': 1, 'name': 'Alice', 'age': 30}
```
---

### 53. Virtual Env

A **virtual environment** is a self-contained directory that contains a Python installation for a particular project. It helps **isolate dependencies** so they don’t conflict between projects.

---

## ✅ Why Use a Virtual Environment?

* Keeps project dependencies separate
* Avoids version conflicts
* Makes deployments and collaboration cleaner

---

## 🔹 Create a Virtual Environment

```bash
python -m venv venv_name
```

Example:

```bash
python -m venv myenv
```

This creates a folder called `myenv/` containing a local Python environment.

---

## 🔹 Activate the Virtual Environment

| OS          | Command                     |
| ----------- | --------------------------- |
| Windows     | `myenv\Scripts\activate`    |
| macOS/Linux | `source myenv/bin/activate` |

You’ll see something like this in your terminal:

```
(myenv) $
```

---

## 🔹 Install Packages Inside It

```bash
pip install package-name
```

Example:

```bash
pip install requests
```

Packages will be installed **only inside** `myenv`.

---

## 🔹 Freeze Installed Packages

```bash
pip freeze > requirements.txt
```

This creates a list of dependencies (great for sharing with others).

---

## 🔹 Reinstall from `requirements.txt`

```bash
pip install -r requirements.txt
```

---

## 🔹 Deactivate the Environment

```bash
deactivate
```

Returns to the system’s default Python environment.

---

## 🧠 Summary

| Task                      | Command                           |
| ------------------------- | --------------------------------- |
| Create environment        | `python -m venv myenv`            |
| Activate (Windows)        | `myenv\Scripts\activate`          |
| Activate (macOS/Linux)    | `source myenv/bin/activate`       |
| Deactivate                | `deactivate`                      |
| Install packages          | `pip install <pkg>`               |
| Export packages           | `pip freeze > requirements.txt`   |
| Install from requirements | `pip install -r requirements.txt` |

---

### 54. Web Scraping

**Web scraping** is the process of **extracting data from websites**. Python offers powerful libraries like `requests` and `BeautifulSoup` to help you scrape web content efficiently.

---

## ✅ Required Libraries

Install them with:

```bash
pip install requests beautifulsoup4
```

---

## 🔹 Step-by-Step Example

```python
import requests
from bs4 import BeautifulSoup

# Step 1: Send a request to the webpage
url = 'https://example.com'
response = requests.get(url)

# Step 2: Parse the HTML content
soup = BeautifulSoup(response.text, 'html.parser')

# Step 3: Extract specific elements
title = soup.title.text
print("Page Title:", title)

# Example: Find all paragraph tags
paragraphs = soup.find_all('p')
for p in paragraphs:
    print(p.text)
```

---

## 🔍 Useful `BeautifulSoup` Methods

| Method                      | Description                                |
| --------------------------- | ------------------------------------------ |
| `soup.title`                | Gets the `<title>` tag                     |
| `soup.find(tag)`            | Finds first occurrence of a tag            |
| `soup.find_all(tag)`        | Finds all occurrences of a tag             |
| `soup.find(id='value')`     | Finds element by ID                        |
| `soup.find(class_='value')` | Finds element by class name                |
| `.text`                     | Gets the text inside a tag                 |
| `.get('href')`              | Gets the value of an attribute (e.g. link) |

---

## 🔗 Example: Get All Links

```python
links = soup.find_all('a')

for link in links:
    href = link.get('href')
    print(href)
```

---

## 🛡️ Responsible Scraping Tips

* Always check the website's `robots.txt`: `https://example.com/robots.txt`
* Avoid overloading servers — use delays between requests:

```python
import time
time.sleep(1)
```

* Use a custom user-agent to identify your bot politely:

```python
headers = {'User-Agent': 'MyScraperBot/1.0'}
response = requests.get(url, headers=headers)
```

---

## 🧠 Summary

| Tool            | Purpose                          |
| --------------- | -------------------------------- |
| `requests`      | Download HTML content            |
| `BeautifulSoup` | Parse and extract data from HTML |

---

### 55. Docstrings

**Docstrings** are special strings used to document **what a function, class, or module does**. They are placed as the **first statement inside** the object (function, class, module).

They help:

* Others understand your code
* Generate documentation automatically
* Improve code readability

---

## 🔹 Basic Function Docstring

```python
def greet(name):
    """Return a greeting for the given name."""
    return f"Hello, {name}!"
```

You can access it with:

```python
print(greet.__doc__)  # Output: Return a greeting for the given name.
```

---

## 🔹 Multi-line Docstring Format (PEP 257)

```python
def divide(a, b):
    """
    Divide two numbers and return the result.

    Parameters:
    a (int or float): Numerator
    b (int or float): Denominator

    Returns:
    float: The result of division

    Raises:
    ZeroDivisionError: If b is zero
    """
    if b == 0:
        raise ZeroDivisionError("Cannot divide by zero.")
    return a / b
```

---

## 🔹 Class Docstring

```python
class Animal:
    """A class representing an animal."""

    def __init__(self, name):
        """Initialize the animal with a name."""
        self.name = name
```

---

## ✅ Best Practices

* Use triple double quotes (`"""doc"""`)
* Be concise but clear
* Mention:

  * Purpose
  * Parameters
  * Return value
  * Exceptions (if any)

---

## 🔹 Tools That Use Docstrings

* IDE tooltips (PyCharm, VS Code)
* Help system: `help(function)`
* Documentation generators (e.g. Sphinx, pdoc)

---

## 🧠 Summary

| Location     | Example Usage           |
| ------------ | ----------------------- |
| Function     | `def func(): """..."""` |
| Class        | `class C: """..."""`    |
| Module (top) | `"""This module..."""`  |

---

### 65. `__name__ == "__main__"`

This line is used to **control the execution** of your code — especially when your script can be **both run directly or imported as a module**.

---

## 🔹 What It Means

```python
if __name__ == "__main__":
    # Run this code only when the script is executed directly
```

---

## ✅ Why Use It?

* Prevents certain code from running when the file is **imported**
* Useful for writing reusable **modules**
* Great for running **tests or main logic** in a controlled way

---

## 🔍 How It Works

Python sets a special built-in variable:

| Condition                  | `__name__` value |
| -------------------------- | ---------------- |
| Script is **run directly** | `"__main__"`     |
| Script is **imported**     | `module_name`    |

---

## 🔧 Example

### File: `greet.py`

```python
def say_hello():
    print("Hello!")

if __name__ == "__main__":
    say_hello()
```

### File: `main.py`

```python
import greet  # Imports without running say_hello()
```

Output:

```
(Only runs when greet.py is executed directly, not when imported.)
```

---

## ✅ Use Case: Entry Point for a Program

```python
def main():
    print("Program is running...")

if __name__ == "__main__":
    main()
```

---

## 🧠 Summary

| Purpose                       | Explanation                                           |
| ----------------------------- | ----------------------------------------------------- |
| Entry point check             | Ensures certain code runs only when executed directly |
| Reusability                   | Keeps modules clean and import-safe                   |
| Common in CLI tools & scripts | Helps define where a program "starts"                 |

---
