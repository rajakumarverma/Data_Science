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

## 22. Tuple

A **tuple** is a collection data type in Python that is:

* **Ordered**
* **Immutable** (cannot be changed after creation)
* Allows **duplicates**
* Can store **mixed data types**

---

## 🔹 Creating a Tuple

```python
my_tuple = (1, 2, 3)
names = ("Alice", "Bob", "Charlie")
mixed = (1, "two", 3.0, True)
single = (5,)      # Note the comma – needed for single-item tuple
empty = ()         # Empty tuple
```

---

## 🔹 Accessing Tuple Elements

```python
print(my_tuple[0])     # 1
print(my_tuple[-1])    # 3
```

---

## 🔹 Tuple Slicing

```python
print(my_tuple[1:])    # (2, 3)
print(my_tuple[:2])    # (1, 2)
```

---

## 🔒 Tuples Are Immutable

You **cannot modify**, **append**, or **remove** elements:

```python
# my_tuple[0] = 10   ❌ TypeError
# my_tuple.append(4) ❌ AttributeError
```

But you can **reassign** the entire tuple:

```python
my_tuple = (4, 5, 6)
```

---

## 🔁 Looping Through a Tuple

```python
for item in my_tuple:
    print(item)
```

---

## 🔹 Tuple Methods

Tuples have **limited methods**:

| Method     | Description                       |
| ---------- | --------------------------------- |
| `count(x)` | Counts how many times `x` appears |
| `index(x)` | Returns the index of first `x`    |

```python
nums = (1, 2, 2, 3)
print(nums.count(2))  # 2
print(nums.index(3))  # 3
```

---

## 🔁 Tuple Packing & Unpacking

```python
# Packing
person = ("Alice", 25, "Engineer")

# Unpacking
name, age, job = person
print(name)  # Alice
print(age)   # 25
```
---

## 23. Set

A **set** is a built-in Python data type used to store **unordered**, **unique** items.
It's useful for removing duplicates and performing **mathematical set operations** like union, intersection, etc.

---

## 🔹 Characteristics of Sets

* ✅ **Unordered** (no index)
* ✅ **Mutable** (can add/remove elements)
* ✅ **No duplicates allowed**
* ❌ **Cannot access by index**
* ✅ **Fast membership testing**

---

## 🔹 Creating a Set

```python
my_set = {1, 2, 3}
empty_set = set()  # NOT {} — that creates a dict
mixed_set = {1, "two", 3.0}
```

---

## 🔹 Duplicate Values Are Ignored

```python
s = {1, 2, 2, 3}
print(s)  # Output: {1, 2, 3}
```

---

## 🔹 Adding and Removing Elements

```python
s = {1, 2}

s.add(3)           # {1, 2, 3}
s.remove(1)        # {2, 3}
s.discard(5)       # No error if 5 not found
s.clear()          # Empty the set
```

---

## 🔹 Set Operations

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)   # Union → {1, 2, 3, 4, 5}
print(a & b)   # Intersection → {3}
print(a - b)   # Difference → {1, 2}
print(a ^ b)   # Symmetric difference → {1, 2, 4, 5}
```

---

## 🔁 Looping Through a Set

```python
for item in {"apple", "banana", "cherry"}:
    print(item)
```

> Output order is unpredictable because sets are unordered.

---

## 🔍 Membership Testing (Fast)

```python
fruits = {"apple", "banana"}
print("apple" in fruits)     # True
print("mango" not in fruits) # True
```

---

## 🆚 Set vs List vs Tuple

| Feature    | List (`[]`) | Tuple (`()`) | Set (`{}`)    |
| ---------- | ----------- | ------------ | ------------- |
| Ordered    | ✅           | ✅            | ❌             |
| Mutable    | ✅           | ❌            | ✅             |
| Duplicates | ✅ Allowed   | ✅ Allowed    | ❌ Not Allowed |
| Indexed    | ✅ Yes       | ✅ Yes        | ❌ No indexing |

---

## 24. Dictionary

A **dictionary** is a built-in Python data type used to store **key–value pairs**.
It is:

* ✅ **Unordered** (as of Python 3.6+, insertion order is preserved)
* ✅ **Mutable** (you can change it)
* ✅ **Indexed by keys, not positions**
* ❌ Keys must be **unique** and **immutable** (strings, numbers, tuples)

---

## 🔹 Creating a Dictionary

```python
person = {
    "name": "Alice",
    "age": 25,
    "is_student": True
}
```

Or using the `dict()` constructor:

```python
person = dict(name="Bob", age=30)
```

---

## 🔹 Accessing Values

```python
print(person["name"])        # Alice
print(person.get("age"))     # 25
print(person.get("email"))   # None (safe way to access)
```

---

## 🔹 Adding / Updating Items

```python
person["email"] = "alice@example.com"  # Add
person["age"] = 26                     # Update
```

---

## 🔹 Removing Items

```python
person.pop("age")         # Removes 'age'
del person["is_student"]  # Removes 'is_student'
person.clear()            # Clears the entire dictionary
```

---

## 🔹 Looping Through a Dictionary

```python
for key in person:
    print(key, person[key])

# Or:
for key, value in person.items():
    print(key, value)
```

---

## 🔹 Dictionary Methods

| Method          | Description                              |
| --------------- | ---------------------------------------- |
| `get(key)`      | Returns value or `None` if key not found |
| `keys()`        | Returns a view of all keys               |
| `values()`      | Returns a view of all values             |
| `items()`       | Returns a view of key–value pairs        |
| `update(dict2)` | Merges `dict2` into current dictionary   |
| `pop(key)`      | Removes key and returns its value        |
| `clear()`       | Empties the dictionary                   |

---

## ✅ Example

```python
student = {
    "name": "John",
    "marks": 85,
    "passed": True
}

print(student["marks"])          # 85
student["marks"] += 5            # Update
print(student.get("age", "N/A")) # N/A
```

---

## 🧠 Nested Dictionary

```python
users = {
    "user1": {"name": "Alice", "age": 25},
    "user2": {"name": "Bob", "age": 30}
}

print(users["user1"]["name"])  # Alice
```
---

## 25. Function

A **function** is a reusable block of code that performs a specific task.
Functions help make code **modular**, **readable**, and **easy to maintain**.

---

## 🔹 Defining a Function

```python
def function_name():
    # code block
```

### ✅ Example:

```python
def greet():
    print("Hello, world!")

greet()  # Call the function
```

---

## 🔹 Function with Parameters

```python
def greet(name):
    print("Hello,", name)

greet("Alice")  # Output: Hello, Alice
```

---

## 🔹 Function with Return Value

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # 8
```

---

## 🔹 Default Parameters

```python
def greet(name="Guest"):
    print("Hello,", name)

greet()         # Hello, Guest
greet("Bob")    # Hello, Bob
```

---

## 🔹 Keyword Arguments

```python
def profile(name, age):
    print(f"Name: {name}, Age: {age}")

profile(age=25, name="Alice")
```
---

## 🧠 Function Scope

* **Local Variable**: Defined inside a function
* **Global Variable**: Defined outside all functions

```python
x = 10  # Global

def show():
    x = 5  # Local
    print(x)

show()     # 5
print(x)   # 10
```

---

## 🧪 Lambda Function (Anonymous Function)

```python
square = lambda x: x * x
print(square(4))  # 16
```

---

## 26. *args and **kwargs

### ⭐ `*args` and `**kwargs` in Python

They allow you to **pass a variable number of arguments** to a function.

---

## 🔹 `*args` (Non-keyword arguments)

* Stands for "**arguments**"
* Collects extra **positional arguments** as a **tuple**

### ✅ Example:

```python
def add_numbers(*args):
    print(args)
    return sum(args)

print(add_numbers(1, 2, 3))   # (1, 2, 3) → 6
```

You can loop through `args`:

```python
def show_names(*args):
    for name in args:
        print("Hello", name)

show_names("Alice", "Bob", "Charlie")
```

---

## 🔹 `**kwargs` (Keyword arguments)

* Stands for "**keyword arguments**"
* Collects extra **named arguments** into a **dictionary**

### ✅ Example:

```python
def show_info(**kwargs):
    print(kwargs)

show_info(name="Alice", age=30)
# Output: {'name': 'Alice', 'age': 30}
```

You can loop through `kwargs`:

```python
def display_details(**kwargs):
    for key, value in kwargs.items():
        print(f"{key} = {value}")

display_details(name="Bob", course="Python", level="Beginner")
```

---

## 🔹 Using Both Together

```python
def demo(a, *args, **kwargs):
    print("a =", a)
    print("args =", args)
    print("kwargs =", kwargs)

demo(1, 2, 3, x=10, y=20)
```

**Output:**

```
a = 1
args = (2, 3)
kwargs = {'x': 10, 'y': 20}
```

---

## 🔁 When to Use

| Use this   | When                                                            |
| ---------- | --------------------------------------------------------------- |
| `*args`    | You don’t know how many **positional** arguments will be passed |
| `**kwargs` | You don’t know how many **keyword** arguments will be passed    |

---

## 27. return Statement

The `return` statement is used in a function to **send a value back** to the caller.
It also **ends** the function's execution.

---

## 🔹 Basic Syntax

```python
def function_name():
    return value
```

---

## ✅ Example 1: Return a Value

```python
def square(num):
    return num * num

result = square(4)
print(result)  # 16
```

---

## ✅ Example 2: Return Multiple Values

```python
def get_info():
    name = "Alice"
    age = 25
    return name, age

n, a = get_info()
print(n)  # Alice
print(a)  # 25
```

Returned values are packaged as a **tuple**:

```python
# Same as:
info = get_info()
print(info)  # ('Alice', 25)
```

---

## 🔹 Without a `return`

If no `return` is used, the function returns `None` by default:

```python
def say_hello():
    print("Hello")

result = say_hello()  # Prints: Hello
print(result)         # None
```

---

## 🔹 Using `return` to End a Function Early

```python
def check_even(n):
    if n % 2 == 0:
        return True
    return False
```

---

## 🧠 Summary

| Purpose of `return`     | Behavior                   |
| ----------------------- | -------------------------- |
| Return a single value   | `return x`                 |
| Return multiple values  | `return x, y, z` → tuple   |
| No return statement     | Returns `None`             |
| Ends function execution | Function stops at `return` |

---

### 28. File Reading (`r`)

### 📂 File Reading in Python (`'r'` mode)

The `'r'` mode is used to **read data from a file** in Python.
This is the **default** mode when opening a file.

---

## 🔹 Basic Syntax

```python
file = open("filename.txt", "r")
# or simply:
file = open("filename.txt")

# Read file content
content = file.read()

# Always close the file
file.close()
```

---

## ✅ Example

```python
file = open("example.txt", "r")

print(file.read())

file.close()
```

---

## 🔹 Best Practice: `with` Statement

Automatically handles file closing:

```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

---

## 🔹 Reading Methods

| Method        | Description                           |
| ------------- | ------------------------------------- |
| `read()`      | Reads the **entire file** as a string |
| `readline()`  | Reads **one line** at a time          |
| `readlines()` | Reads **all lines** into a list       |

### Example:

```python
with open("example.txt", "r") as f:
    print(f.readline())   # Reads first line
    print(f.readlines())  # Reads remaining lines as list
```

---

## 🔹 Looping Through Lines

```python
with open("example.txt", "r") as f:
    for line in f:
        print(line.strip())  # strip() removes \n
```

---

## 🔍 What if File Doesn't Exist?

Opening a non-existent file in `'r'` mode causes an error:

```python
with open("missing.txt", "r") as f:
    # FileNotFoundError
```

Handle with `try` block:

```python
try:
    with open("missing.txt", "r") as f:
        print(f.read())
except FileNotFoundError:
    print("File not found!")
```
---

### 29. File Writing (`w`)

The `'w'` mode is used to **write data to a file**.
It **creates** the file if it doesn't exist, and **overwrites** it if it does.

---

## 🔹 Basic Syntax

```python
file = open("filename.txt", "w")
file.write("Hello, world!")
file.close()
```

---

## ✅ Example

```python
with open("output.txt", "w") as f:
    f.write("This is line 1.\n")
    f.write("This is line 2.\n")
```

📁 This will create or overwrite `output.txt` with:

```
This is line 1.
This is line 2.
```

---

## ⚠️ Overwriting Behavior

```python
with open("data.txt", "w") as f:
    f.write("First write.\n")

# Opening in 'w' mode again overwrites it:
with open("data.txt", "w") as f:
    f.write("This will erase previous content.")
```

---

## 🔹 Writing Multiple Lines

You can use `.writelines()` with a list of strings:

```python
lines = ["Line A\n", "Line B\n", "Line C\n"]
with open("list_output.txt", "w") as f:
    f.writelines(lines)
```

---

## 🧠 Reminder

Always use `\n` for line breaks — Python doesn't add them automatically.

---

## 🔄 Summary: File Modes

| Mode  | Action                        |
| ----- | ----------------------------- |
| `'r'` | Read (file must exist)        |
| `'w'` | Write (creates or overwrites) |
| `'a'` | Append (adds to end of file)  |
| `'x'` | Create (fails if file exists) |

---

### 30. Append to File (`a`)

### 📌 Append to File in Python (`'a'` mode)

The `'a'` mode is used to **append data** to the **end of an existing file** without deleting its current content.
If the file doesn’t exist, it will be **created**.

---

## 🔹 Basic Syntax

```python
file = open("filename.txt", "a")
file.write("New content\n")
file.close()
```

---

## ✅ Example

```python
with open("log.txt", "a") as f:
    f.write("Log entry 1\n")
    f.write("Log entry 2\n")
```

Each time you run this code, it will **add** more lines at the end of `log.txt`.

---

## 🔹 Appending Multiple Lines

```python
lines = ["Line A\n", "Line B\n"]
with open("notes.txt", "a") as f:
    f.writelines(lines)
```

---

## 🧠 Tip: Always Use `\n` for New Lines

Python’s `write()` and `writelines()` won’t add line breaks automatically.
You must include `\n` at the end of each line yourself.

---

## 🔄 Compare File Modes

| Mode  | Description                   |
| ----- | ----------------------------- |
| `'r'` | Read (file must exist)        |
| `'w'` | Write (overwrites file)       |
| `'a'` | Append (adds to end of file)  |
| `'x'` | Create (fails if file exists) |

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
