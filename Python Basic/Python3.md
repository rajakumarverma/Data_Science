### 31. Try/Except

The `try` / `except` block is used for **exception handling**.
It lets your program **catch and handle errors** without crashing.

---

## 🔹 Basic Syntax

```python
try:
    # code that might cause an error
except:
    # code that runs if there's an error
```

---

## ✅ Example

```python
try:
    x = int(input("Enter a number: "))
    print("You entered:", x)
except:
    print("That’s not a valid number!")
```

---

## 🔹 Catching Specific Exceptions

It's best to catch specific errors like `ValueError`, `ZeroDivisionError`, etc.

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("You can't divide by zero!")
```

---

## 🔹 Multiple Except Blocks

```python
try:
    x = int(input("Enter a number: "))
    y = 10 / x
except ValueError:
    print("Not a valid integer!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

---

## 🔹 Using `else` and `finally`

```python
try:
    num = int(input("Enter number: "))
except ValueError:
    print("Invalid!")
else:
    print("You entered:", num)
finally:
    print("Try/except block finished.")
```

* `else`: Runs if **no exception** occurs
* `finally`: Always runs **no matter what** (used for cleanup)

---

## 🔍 Common Exceptions

| Exception           | Reason                               |
| ------------------- | ------------------------------------ |
| `ValueError`        | Wrong data type (e.g., `int("abc")`) |
| `ZeroDivisionError` | Division by zero                     |
| `FileNotFoundError` | File does not exist                  |
| `TypeError`         | Wrong data type in operation         |
| `KeyError`          | Dictionary key not found             |
| `IndexError`        | List index out of range              |

---

## ✅ Good Practice

Always handle **specific** exceptions first, then use a general one if needed:

```python
try:
    # risky code
except (ValueError, TypeError) as e:
    print("Handled:", e)
except Exception as e:
    print("Unexpected error:", e)
```
---

### 32. Finally Clause

The `finally` block is used to **guarantee the execution** of code —
whether or not an exception occurs in the `try` block.

---

## 🔹 Syntax

```python
try:
    # risky code
except:
    # handle exception
finally:
    # always runs
```

---

## ✅ Example 1: No Error Occurs

```python
try:
    print("Try block runs")
    x = 10 / 2
except:
    print("Exception occurred")
finally:
    print("Finally block always runs")
```

**Output:**

```
Try block runs  
Finally block always runs
```

---

## ✅ Example 2: Error Occurs

```python
try:
    print("Trying division by zero")
    x = 10 / 0
except ZeroDivisionError:
    print("Caught a ZeroDivisionError")
finally:
    print("Cleanup code runs here")
```

**Output:**

```
Trying division by zero  
Caught a ZeroDivisionError  
Cleanup code runs here
```

---

## 🧹 When to Use `finally`

Use `finally` for **cleanup tasks**, like:

* Closing a file
* Closing a database connection
* Releasing resources

### ✅ Example: Closing a File Safely

```python
try:
    f = open("file.txt", "r")
    content = f.read()
except FileNotFoundError:
    print("File not found.")
finally:
    f.close()
    print("File closed.")
```

---

## 🔄 Summary

| Block     | Runs When?                          |
| --------- | ----------------------------------- |
| `try`     | When you want to attempt risky code |
| `except`  | If an error occurs                  |
| `finally` | Always, no matter what              |

---

### 33. Raise Exception

The `raise` statement lets you **manually trigger an exception**.
You can use it to enforce conditions, create custom errors, or stop execution when something is wrong.

---

## 🔹 Basic Syntax

```python
raise ExceptionType("Custom error message")
```

---

## ✅ Example 1: Raise a `ValueError`

```python
age = -5

if age < 0:
    raise ValueError("Age cannot be negative")
```

**Output:**

```
ValueError: Age cannot be negative
```

---

## ✅ Example 2: Inside a Function

```python
def divide(x, y):
    if y == 0:
        raise ZeroDivisionError("You can't divide by zero")
    return x / y

print(divide(10, 0))  # Triggers error
```

---

## ✅ Example 3: Using `raise` in `try`/`except`

```python
try:
    raise RuntimeError("Something went wrong")
except RuntimeError as err:
    print("Caught an error:", err)
```

---

## 🔹 Raising Built-in Exceptions

You can raise any built-in exception like:

* `TypeError`
* `ValueError`
* `IndexError`
* `KeyError`
* `ZeroDivisionError`

---

## 🔹 Raising Custom Exceptions

You can define your **own exception class**:

```python
class MyError(Exception):
    pass

raise MyError("This is a custom error")
```

---

## 🧠 When to Use `raise`

* To **validate user input**
* To **stop a program** if certain conditions fail
* In APIs or libraries, to signal **unexpected usage**

---

### 34. Class & Object

Python is an **object-oriented programming** (OOP) language.
Classes and objects are the core building blocks of OOP.

---

## 🔹 What is a **Class**?

A **class** is a **blueprint** for creating objects.
It defines **attributes** (variables) and **methods** (functions) that the objects will have.

### ✅ Example:

```python
class Person:
    def __init__(self, name, age):  # Constructor
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello, my name is {self.name}.")
```

---

## 🔹 What is an **Object**?

An **object** is an **instance** of a class.

### ✅ Creating an Object:

```python
p1 = Person("Alice", 25)  # Object of Person class
p1.greet()  # Output: Hello, my name is Alice.
```

---

## 🔹 `__init__()` Method (Constructor)

* A **special method** that runs automatically when an object is created.
* It’s used to **initialize attributes**.

```python
def __init__(self, name):
    self.name = name
```

---

## 🔹 `self` Keyword

* Refers to the **current object**.
* Used to access attributes and methods from within the class.

---

## 🔹 Accessing Attributes & Methods

```python
print(p1.name)     # Alice
print(p1.age)      # 25
p1.greet()         # Hello, my name is Alice.
```

---

## 🧠 Summary

| Term       | Description                       |
| ---------- | --------------------------------- |
| `class`    | Blueprint for creating objects    |
| `object`   | Instance of a class               |
| `__init__` | Constructor for initializing data |
| `self`     | Refers to the current instance    |

---

### Bonus: Example with Multiple Methods

```python
class Calculator:
    def __init__(self, a, b):
        self.a = a
        self.b = b

    def add(self):
        return self.a + self.b

    def multiply(self):
        return self.a * self.b

c = Calculator(3, 5)
print(c.add())        # 8
print(c.multiply())   # 15
```
---

### 35. Class Methods

A **class method** is a method that belongs to the **class itself**, not just to instances (objects).
It can **access and modify class-level data**, and is defined using the `@classmethod` decorator.

---

## 🔹 Syntax

```python
class MyClass:
    @classmethod
    def my_class_method(cls, args):
        # cls refers to the class, not the instance
```

---

## ✅ Example

```python
class Dog:
    species = "Canine"  # Class variable

    def __init__(self, name):
        self.name = name

    @classmethod
    def get_species(cls):
        return f"All dogs are {cls.species}"

# Usage
print(Dog.get_species())  # All dogs are Canine
```

* `cls` is like `self`, but refers to the **class**, not the **instance**.
* You can call class methods on both the class and its objects.

---

## 🔹 Modify Class Variable Using Class Method

```python
class Counter:
    count = 0

    @classmethod
    def increment(cls):
        cls.count += 1

Counter.increment()
Counter.increment()
print(Counter.count)  # 2
```

---

## 🔹 Difference: `@classmethod` vs `@staticmethod` vs instance methods

| Type            | Access to `self` | Access to `cls` | Access class/instance data |
| --------------- | ---------------- | --------------- | -------------------------- |
| Instance Method | ✅ Yes            | ❌ No            | ✅ Yes                      |
| Class Method    | ❌ No             | ✅ Yes           | ✅ Class only               |
| Static Method   | ❌ No             | ❌ No            | ❌ (Utility method)         |

---

## 🔹 Use Cases for `@classmethod`

* Creating factory methods (alternative constructors)
* Accessing or modifying **class-level data**
* Defining behaviors shared across all instances

---

### ✅ Factory Method Example

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    @classmethod
    def from_birth_year(cls, name, birth_year):
        from datetime import datetime
        current_year = datetime.now().year
        age = current_year - birth_year
        return cls(name, age)

p = Person.from_birth_year("Alice", 2000)
print(p.name, p.age)
```
---

### 36. Inheritance

**Inheritance** allows a class (called the **child** or **derived** class) to **inherit** attributes and methods from another class (called the **parent** or **base** class).
It promotes **code reuse**, **organization**, and **extensibility**.

---

## 🔹 Basic Syntax

```python
class Parent:
    # base class
    pass

class Child(Parent):
    # derived class
    pass
```

---

## ✅ Simple Example

```python
class Animal:
    def speak(self):
        print("This animal makes a sound.")

class Dog(Animal):
    def bark(self):
        print("The dog barks.")

# Usage
d = Dog()
d.speak()  # Inherited from Animal
d.bark()   # Defined in Dog
```

---

## 🔹 `super()` Function

Use `super()` to call the **parent class’s constructor** or methods.

```python
class Person:
    def __init__(self, name):
        self.name = name

class Student(Person):
    def __init__(self, name, grade):
        super().__init__(name)       # Call Person's __init__
        self.grade = grade
```

---

## 🔹 Types of Inheritance

| Type             | Description                                | Example                      |
| ---------------- | ------------------------------------------ | ---------------------------- |
| **Single**       | One child inherits from one parent         | `class B(A):`                |
| **Multilevel**   | A class inherits from a child class        | `class C(B):`                |
| **Multiple**     | A class inherits from **multiple** parents | `class C(A, B):`             |
| **Hierarchical** | Multiple classes inherit from one parent   | `class B(A):`, `class C(A):` |

---

## ✅ Example: Multilevel Inheritance

```python
class Vehicle:
    def start(self):
        print("Vehicle started")

class Car(Vehicle):
    def drive(self):
        print("Car is driving")

class ElectricCar(Car):
    def charge(self):
        print("Charging battery")

e = ElectricCar()
e.start()   # From Vehicle
e.drive()   # From Car
e.charge()  # From ElectricCar
```

---

## 🧠 Benefits of Inheritance

* Reuse code
* Easier to manage large codebases
* Supports polymorphism and method overriding

---

### 37. `super()`

The `super()` function is used to **call a method from the parent class**, most commonly the `__init__()` constructor.
It’s a key tool when working with **inheritance**.

---

## 🔹 Why use `super()`?

* Avoids manually referencing the parent class
* Makes your code **cleaner**, especially in **multiple inheritance**
* Ensures proper **method resolution order (MRO)**

---

## ✅ Basic Example

```python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)  # calls Animal's __init__
        self.breed = breed

d = Dog("Buddy", "Labrador")
print(d.name)   # Buddy
print(d.breed)  # Labrador
```

---

## 🔹 Without `super()`

```python
class Dog(Animal):
    def __init__(self, name, breed):
        Animal.__init__(self, name)  # works, but less flexible
        self.breed = breed
```

✅ Works, but hard-coding the parent class (`Animal`) is discouraged.

---

## 🔹 `super()` in Method Overriding

```python
class A:
    def greet(self):
        print("Hello from A")

class B(A):
    def greet(self):
        super().greet()
        print("Hello from B")

b = B()
b.greet()
```

**Output:**

```
Hello from A  
Hello from B
```

---

## 🔹 In Multiple Inheritance

```python
class A:
    def show(self):
        print("A")

class B(A):
    def show(self):
        super().show()
        print("B")

class C(B):
    def show(self):
        super().show()
        print("C")

c = C()
c.show()
```

**Output (MRO-based):**

```
A  
B  
C
```

---

## 🧠 Summary

| Feature   | Description                                  |
| --------- | -------------------------------------------- |
| `super()` | Calls a method from the parent class         |
| Use case  | Mostly in constructors or overridden methods |
| Benefit   | Avoids hardcoding, follows MRO               |

---

### 38. `__str__()` Method

The `__str__()` method is a **special (magic) method** in Python used to define a **human-readable string representation** of an object.

It gets called automatically when you use:

* `print(object)`
* `str(object)`

---

## 🔹 Basic Syntax

```python
class ClassName:
    def __str__(self):
        return "String representation"
```

---

## ✅ Example

```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author

    def __str__(self):
        return f"'{self.title}' by {self.author}"

b = Book("1984", "George Orwell")
print(b)
```

**Output:**

```
'1984' by George Orwell
```

Without `__str__()`, printing `b` would show something like:

```
<__main__.Book object at 0x104f3eb80>
```

---

## 🔍 Difference: `__str__()` vs `__repr__()`

| Method       | Purpose                             | Used By             |
| ------------ | ----------------------------------- | ------------------- |
| `__str__()`  | For users – readable output         | `print()` / `str()` |
| `__repr__()` | For developers – unambiguous output | `repr()` / debugger |

```python
def __repr__(self):
    return f"Book('{self.title}', '{self.author}')"
```

---

## 🧠 Tip: Always Define `__str__()` in Your Classes

It makes debugging, logging, and displaying data much easier and clearer.

---

### 42. Importing Modules

Use code from other files/libraries.

```python
import math
print(math.sqrt(16))  # 4.0
```

---

### 39. `from ... import`

The `from ... import` statement is used to **import specific parts** (functions, classes, variables) from a module, rather than importing the whole module.

---

## 🔹 Basic Syntax

```python
from module_name import item_name
```

This lets you use `item_name` **directly**, without the module prefix.

---

## ✅ Example 1: Importing a Function

```python
from math import sqrt

print(sqrt(16))  # Output: 4.0
```

---

## ✅ Example 2: Importing Multiple Items

```python
from math import sqrt, pi

print(sqrt(25))  # 5.0
print(pi)        # 3.141592653589793
```

---

## ✅ Example 3: Import with Alias

```python
from math import sqrt as square_root

print(square_root(9))  # 3.0
```

---

## 🔹 Wildcard Import (⚠️ Not Recommended)

```python
from math import *
print(sin(0))  # 0.0
```

> ❗ This imports *everything* in the module. Avoid in large projects to prevent name conflicts.

---

## 🔹 Importing from Your Own File

Given a file `utils.py` with:

```python
def greet(name):
    return f"Hello, {name}!"
```

You can import it in another file:

```python
from utils import greet

print(greet("Alice"))  # Hello, Alice!
```

---

## 🧠 Summary

| Statement                      | Purpose                             |
| ------------------------------ | ----------------------------------- |
| `import module`                | Imports the entire module           |
| `from module import name`      | Imports a specific item             |
| `from module import name as x` | Imports with an alias               |
| `from module import *`         | Imports everything (use cautiously) |

---

### 40. Creating Modules

A **module** is simply a **Python file** (`.py`) that contains **functions, classes, or variables** that you can reuse in other Python files.

This is great for organizing and reusing code across projects.

---

## 🔹 Step-by-Step: Creating and Using a Module

### ✅ Step 1: Create a Python file (your module)

**`mymath.py`**

```python
# This is your custom module

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y
```

---

### ✅ Step 2: Import and use the module in another file

**`main.py`**

```python
import mymath

print(mymath.add(5, 3))       # Output: 8
print(mymath.subtract(10, 4)) # Output: 6
```

---

## 🔹 Using `from ... import ...` with Your Module

```python
from mymath import add

print(add(2, 3))  # Output: 5
```

---

## 🔹 Adding Variables and Classes to a Module

**`info.py`**

```python
name = "Python"
version = 3.11

class Greet:
    def say_hello(self):
        print("Hello from module!")
```

**`main.py`**

```python
from info import name, version, Greet

print(name)       # Python
print(version)    # 3.11

g = Greet()
g.say_hello()     # Hello from module!
```

---

## 🧠 Summary

| Concept                | Description                     |
| ---------------------- | ------------------------------- |
| Module                 | A `.py` file with code to reuse |
| `import module`        | Import the whole module         |
| `from module import x` | Import specific parts           |
| Reusability            | Keeps code modular and clean    |

---

### 41. pip / Package Install

`pip` is the **standard package manager for Python**.
It lets you **install**, **upgrade**, and **uninstall** third-party libraries and tools from [PyPI](https://pypi.org).

---

## 🔹 Basic Commands

| Command                              | Description                  |
| ------------------------------------ | ---------------------------- |
| `pip install package_name`           | Install a package            |
| `pip uninstall package_name`         | Remove a package             |
| `pip install --upgrade package_name` | Upgrade a package            |
| `pip list`                           | Show installed packages      |
| `pip show package_name`              | Show details about a package |

---

## ✅ Example: Install `requests`

```bash
pip install requests
```

Use it in Python:

```python
import requests

response = requests.get("https://api.github.com")
print(response.status_code)
```

---

## 🔹 Installing Specific Versions

```bash
pip install numpy==1.24.0
```

---

## 🔹 Install from a `requirements.txt` file

This file lists all dependencies:

**`requirements.txt`**

```
requests
pandas>=1.4.0
flask==2.3.2
```

Then install everything at once:

```bash
pip install -r requirements.txt
```

---

## 🔹 Uninstall a Package

```bash
pip uninstall requests
```

---

## 🔹 Check if pip is installed

```bash
pip --version
```

If not, install it using:

```bash
python -m ensurepip --upgrade
```

---

## 🧠 Tip: Use a Virtual Environment

To avoid messing with global Python packages, use:

```bash
python -m venv env
source env/bin/activate   # On Mac/Linux
env\Scripts\activate      # On Windows
```

Then install packages locally.

---

### 42. Lambda Function

A **lambda function** is a **small, anonymous function** in Python.
It can have **any number of arguments**, but only **one expression**.

---

## 🔹 Syntax

```python
lambda arguments: expression
```

* The expression is **automatically returned**.
* Often used when a simple function is needed **temporarily or inline**.

---

## ✅ Example 1: Add two numbers

```python
add = lambda x, y: x + y
print(add(3, 5))  # Output: 8
```

---

## ✅ Example 2: Square a number

```python
square = lambda n: n * n
print(square(4))  # Output: 16
```

---

## ✅ Example 3: Use with `map()`

```python
nums = [1, 2, 3, 4]
squared = list(map(lambda x: x**2, nums))
print(squared)  # Output: [1, 4, 9, 16]
```

---

## ✅ Example 4: Use with `filter()`

```python
nums = [1, 2, 3, 4, 5]
even = list(filter(lambda x: x % 2 == 0, nums))
print(even)  # Output: [2, 4]
```

---

## ✅ Example 5: Use with `sorted()` and `key`

```python
students = [("Alice", 85), ("Bob", 92), ("Charlie", 78)]
# Sort by score
sorted_students = sorted(students, key=lambda x: x[1], reverse=True)
print(sorted_students)
```

## ✅ Example 6: Use with `reduce()`

```python
from functools import reduce
nums = [1, 2, 3, 4]
total = reduce(lambda x, y: x + y, nums)
print(total)  # 10
```

---

## 🧠 When to Use Lambda

✅ Use for:

* One-liners
* Short throwaway functions
* Functional programming (`map`, `filter`, `reduce`)

❌ Avoid for:

* Complex logic
* Reusability (use `def` instead)

---

### 43. List Comprehension

**List comprehension** is a concise way to create lists using a **single line of code**.
It's faster and cleaner than using a traditional `for` loop.

---

## 🔹 Basic Syntax

```python
[expression for item in iterable]
```

### ✅ With Condition:

```python
[expression for item in iterable if condition]
```

---

## ✅ Example 1: Squares of Numbers

```python
squares = [x**2 for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```

---

## ✅ Example 2: Filter Even Numbers

```python
evens = [x for x in range(10) if x % 2 == 0]
print(evens)  # Output: [0, 2, 4, 6, 8]
```

---

## ✅ Example 3: Convert to Uppercase

```python
words = ["apple", "banana", "cherry"]
uppercased = [word.upper() for word in words]
print(uppercased)  # ['APPLE', 'BANANA', 'CHERRY']
```

---

## ✅ Example 4: Nested Loops (2D Comprehension)

```python
pairs = [(x, y) for x in [1, 2] for y in [3, 4]]
print(pairs)  # [(1, 3), (1, 4), (2, 3), (2, 4)]
```

---

## ✅ Example 5: If/Else Inside List Comprehension

```python
labels = ["even" if x % 2 == 0 else "odd" for x in range(5)]
print(labels)  # ['even', 'odd', 'even', 'odd', 'even']
```

---

## 🧠 Benefits

* More **concise** and **readable**
* Often **faster** than using loops
* Great for filtering, transforming, or flattening lists

---

### 44. Dictionary Comprehension

**Dictionary comprehension** allows you to create a new dictionary by writing **key-value pairs in a single line**, similar to list comprehension.

---

## 🔹 Basic Syntax

```python
{key: value for item in iterable}
```

### ✅ With Condition:

```python
{key: value for item in iterable if condition}
```

---

## ✅ Example 1: Squares Dictionary

```python
squares = {x: x**2 for x in range(5)}
print(squares)  # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

---

## ✅ Example 2: Convert Two Lists to Dict

```python
keys = ['a', 'b', 'c']
values = [1, 2, 3]

combined = {k: v for k, v in zip(keys, values)}
print(combined)  # {'a': 1, 'b': 2, 'c': 3}
```

---

## ✅ Example 3: Filter Items in a Dict

```python
original = {'apple': 10, 'banana': 3, 'cherry': 15}
filtered = {k: v for k, v in original.items() if v > 5}
print(filtered)  # {'apple': 10, 'cherry': 15}
```

---

## ✅ Example 4: Swap Keys and Values

```python
data = {'a': 1, 'b': 2}
swapped = {v: k for k, v in data.items()}
print(swapped)  # {1: 'a', 2: 'b'}
```

---

## ✅ Example 5: Add Condition with If/Else

```python
nums = range(5)
labels = {x: ("even" if x % 2 == 0 else "odd") for x in nums}
print(labels)  # {0: 'even', 1: 'odd', 2: 'even', 3: 'odd', 4: 'even'}
```

---

## 🧠 Summary

| Feature              | Benefit                          |
| -------------------- | -------------------------------- |
| One-line dicts       | Clean, readable code             |
| Filters & transforms | Easily filter or modify items    |
| Fast and Pythonic    | Better performance in many cases |

---
