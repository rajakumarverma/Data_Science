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

## 3. Data Types

Python has several **built-in data types** used to store different kinds of values. Here's an overview:

---

### 📦 1. **Basic Data Types**

| Type    | Example         | Description                      |
| ------- | --------------- | -------------------------------- |
| `int`   | `10`, `-5`      | Integer numbers                  |
| `float` | `3.14`, `-0.01` | Decimal (floating-point) numbers |
| `str`   | `'Hello'`       | Text (string)                    |
| `bool`  | `True`, `False` | Boolean values (True or False)   |

```python
a = 10        # int
b = 3.14      # float
c = "Python"  # str
d = True      # bool
```

---

### 📚 2. **Collection Data Types**

| Type    | Example                        | Description                      |
| ------- | ------------------------------ | -------------------------------- |
| `list`  | `[1, 2, 3]`                    | Ordered, changeable collection   |
| `tuple` | `(1, 2, 3)`                    | Ordered, unchangeable collection |
| `set`   | `{1, 2, 3}`                    | Unordered, no duplicates         |
| `dict`  | `{"name": "Alice", "age": 25}` | Key-value pairs                  |

```python
my_list = [1, 2, 3]                 # list
my_tuple = (1, 2, 3)                # tuple
my_set = {1, 2, 3}                  # set
my_dict = {"name": "Alice", "age": 25}  # dict
```

---

### 🔧 3. **Special Types**

| Type       | Example  | Description                             |
| ---------- | -------- | --------------------------------------- |
| `NoneType` | `None`   | Represents the absence of a value       |
| `complex`  | `3 + 4j` | Complex numbers (used in advanced math) |

```python
x = None       # NoneType
z = 3 + 4j     # complex
```

---

## 🧪 4. **Type Checking**

In Python, you can check the **type** of any variable using the built-in `type()` function.

---

## ✅ Basic Syntax

```python
type(variable)
```

### 🔹 Example:

```python
x = 10
print(type(x))  # <class 'int'>

name = "Alice"
print(type(name))  # <class 'str'>

pi = 3.14
print(type(pi))  # <class 'float'>

is_valid = True
print(type(is_valid))  # <class 'bool'>
```

---

## 🧠 Use `isinstance()` for Type Checking (Preferred in Conditional Logic)

`isinstance(object, type)` checks if an object is an instance of a certain type (or tuple of types):

### 🔹 Example:

```python
x = 10

if isinstance(x, int):
    print("x is an integer")
else:
    print("x is not an integer")
```

### 🔹 Multiple types:

```python
value = "123"
if isinstance(value, (int, float, str)):
    print("value is a number or a string")
```

---

## 💡 Difference Between `type()` and `isinstance()`

| Function           | Use Case                                               | Notes                        |
| ------------------ | ------------------------------------------------------ | ---------------------------- |
| `type(x)`          | Returns the exact type of `x`                          | Doesn’t consider inheritance |
| `isinstance(x, T)` | Checks if `x` is an instance of `T` or subclass of `T` | Preferred in conditionals    |


---

## 5. Type Casting

### 🔁 Type Casting in Python (Type Conversion)

**Type casting** means converting one data type into another. Python provides **built-in functions** for this.

---

## 🔹 Common Type Casting Functions

| Function   | Converts To | Example                           |
| ---------- | ----------- | --------------------------------- |
| `int(x)`   | Integer     | `int("5")` → `5`                  |
| `float(x)` | Float       | `float("3.14")` → `3.14`          |
| `str(x)`   | String      | `str(100)` → `"100"`              |
| `bool(x)`  | Boolean     | `bool("")` → `False`              |
| `list(x)`  | List        | `list("abc")` → `['a', 'b', 'c']` |
| `tuple(x)` | Tuple       | `tuple([1, 2])` → `(1, 2)`        |
| `set(x)`   | Set         | `set([1, 2, 2])` → `{1, 2}`       |

---

## ✅ Examples

```python
# To integer
print(int("10"))       # 10
print(int(3.99))        # 3 (decimal part removed)

# To float
print(float("4.5"))    # 4.5
print(float(2))        # 2.0

# To string
print(str(123))        # '123'
print(str(True))       # 'True'

# To boolean
print(bool(""))        # False
print(bool("hello"))   # True
print(bool(0))         # False
print(bool(1))         # True

# To list
print(list("abc"))     # ['a', 'b', 'c']
print(list((1, 2)))    # [1, 2]
```

---

## ⚠️ Things to Watch Out For

1. **Invalid conversions raise errors:**

   ```python
   int("abc")     # ValueError
   float("hello") # ValueError
   ```

2. **`bool()` follows these rules:**

   * `False`: `0`, `0.0`, `''`, `[]`, `{}`, `None`
   * `True`: everything else

---

## 6. Input from User

Python uses the **`input()`** function to take input from the user via the keyboard.

---

## 🔹 Basic Syntax

```python
variable = input("Prompt message: ")
```

> This always returns a **string**!

---

### ✅ Example:

```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
```

**Output:**

```
Enter your name: Alice
Hello, Alice!
```

---

## 🔁 Convert Input to Other Types (Type Casting)

Since `input()` returns a **string**, you must convert it if you want a number or boolean.

### 🔹 Example: Get Integer Input

```python
age = int(input("Enter your age: "))
print("You will be", age + 1, "next year.")
```

### 🔹 Example: Get Float Input

```python
price = float(input("Enter price: "))
print("Total with tax:", price * 1.15)
```

### 🔹 Example: Boolean Input

```python
response = input("Do you agree? (yes/no): ")
is_agree = response.lower() == "yes"
print("Agreed:", is_agree)
```
---

## 7. Output Print


The `print()` function is used to **display output to the screen**.

---

## 🔹 Basic Syntax

```python
print(value1, value2, ..., sep=' ', end='\n')
```

* `value1, value2, ...`: Items to print
* `sep`: Separator between values (default is space `' '`)
* `end`: What to print at the end (default is newline `'\n'`)

---

## ✅ Examples

### 🔸 Print a single value

```python
print("Hello, World!")
```

### 🔸 Print multiple values

```python
name = "Alice"
age = 25
print(name, age)
# Output: Alice 25
```

---

## 🔹 Formatting Output

### 1. **f-strings** (Recommended in Python 3.6+)

```python
name = "Bob"
score = 90
print(f"{name} scored {score} points.")
```

### 2. **`str.format()` method**

```python
print("{} scored {} points.".format(name, score))
```

---

## 🔹 Custom Separators and Endings

### 🔸 `sep` (separator between values)

```python
print("Python", "Java", "C++", sep=", ")
# Output: Python, Java, C++
```

### 🔸 `end` (what to print at the end)

```python
print("Loading", end="...")
print("Done!")
# Output: Loading...Done!
```

---

## 🔹 Printing Without a Newline

```python
print("Hello", end=" ")
print("World")
# Output: Hello World
```

---

## 🧠 Fun Example

```python
name = input("Enter your name: ")
print(f"Welcome, {name}! 🎉")
```
---

## 8. String Indexing

**String indexing** allows you to access individual characters in a string using their **position (index)**.

---

## 🔹 How Indexing Works

In Python, strings are ordered sequences of characters.
Each character has a position (index), starting from **0**.

```python
text = "Python"
# Index:    0 1 2 3 4 5
# Reverse: -6-5-4-3-2-1
```

---

## ✅ Accessing Characters

```python
text = "Python"
print(text[0])   # P
print(text[3])   # h
print(text[-1])  # n (last character)
```

---

## 🛑 Index Out of Range

Accessing an index that doesn't exist will raise an error:

```python
print(text[10])  # IndexError
```

---

## 🔄 Looping Through a String (Optional)

```python
for char in "Hi":
    print(char)
```

---

## 🔍 Use Case: First and Last Letters

```python
word = "apple"
print("First:", word[0])
print("Last:", word[-1])
```

---

## 🔐 Strings Are Immutable

You **cannot** change a character by index directly:

```python
text = "Hello"
# text[0] = "Y"  ❌ This gives TypeError
```

But you can create a new string:

```python
text = "Hello"
new_text = "Y" + text[1:]  # "Yello"
print(new_text)
```
---

## 9. String Slicing

**String slicing** allows you to extract a part (substring) of a string using **start**, **end**, and **step** values.

---

## 🔹 Syntax

```python
string[start:end:step]
```

* `start`: index to begin (inclusive)
* `end`: index to stop (exclusive)
* `step`: how many steps to move (optional)

---

## ✅ Examples

```python
text = "Python"

print(text[0:2])     # 'Py'      (index 0 and 1)
print(text[1:4])     # 'yth'     (index 1 to 3)
print(text[:3])      # 'Pyt'     (from start to index 2)
print(text[3:])      # 'hon'     (from index 3 to end)
print(text[:])       # 'Python'  (full copy)
```

---

## 🔄 Step Slicing

```python
print(text[::2])     # 'Pto'  (every 2nd character)
print(text[::-1])    # 'nohtyP' (reversed string)
```

---

## 🔍 Negative Indexes Work Too

```python
print(text[-4:-1])   # 'tho'
```

---

## 📦 Real Example

```python
word = "Programming"
print(word[3:8])     # 'gramm'
print(word[-5:])     # 'mming'
print(word[::-1])    # 'gnimmargorP'
```

---

## ❗ Remember

* `text[a:b]` gives characters from index `a` to `b-1`
* It doesn't raise an error if indexes go out of range:

  ```python
  print(text[0:100])  # returns up to end if 100 is too big
  ```
---

## 10. String Methods

Python provides **built-in methods** to work with strings easily. These methods do **not change the original string** (strings are immutable); they return **new strings**.

---

## 🔹 Commonly Used String Methods

| Method              | Description                             | Example                                  |
| ------------------- | --------------------------------------- | ---------------------------------------- |
| `lower()`           | Converts to lowercase                   | `"PYTHON".lower()` → `'python'`          |
| `upper()`           | Converts to uppercase                   | `"python".upper()` → `'PYTHON'`          |
| `title()`           | Capitalizes first letter of each word   | `"hello world".title()`                  |
| `strip()`           | Removes leading/trailing whitespace     | `"  hello  ".strip()` → `'hello'`        |
| `replace(old, new)` | Replaces substring                      | `"car".replace("c", "b")` → `'bar'`      |
| `find(sub)`         | Returns index of first occurrence       | `"hello".find("l")` → `2`                |
| `count(sub)`        | Counts occurrences                      | `"hello".count("l")` → `2`               |
| `startswith(sub)`   | Checks if starts with substring         | `"hello".startswith("he")`               |
| `endswith(sub)`     | Checks if ends with substring           | `"hello".endswith("lo")`                 |
| `split(delimiter)`  | Splits into a list                      | `"a,b,c".split(",")` → `['a', 'b', 'c']` |
| `join(iterable)`    | Joins elements with string as separator | `"-".join(['a','b'])` → `'a-b'`          |

---

## ✅ Examples

```python
text = "  Python Programming  "

print(text.lower())        # '  python programming  '
print(text.strip())        # 'Python Programming'
print(text.title())        # 'Python Programming'
print(text.replace("Python", "Java"))  # '  Java Programming  '
print(text.find("Prog"))   # 9
```

---

## 🔄 Example: Splitting and Joining

```python
sentence = "apple,banana,grape"
fruits = sentence.split(",")     # ['apple', 'banana', 'grape']
print(fruits)

joined = "-".join(fruits)        # 'apple-banana-grape'
print(joined)
```

---

## ✅ Boolean String Methods (Return True/False)

```python
text = "Hello123"

print(text.isalpha())    # False (contains digits)
print(text.isdigit())    # False
print("123".isdigit())   # True
print("abc".isalpha())   # True
```
---

## 11. Arithmetic Operators

Python supports all basic **arithmetic operations** using special symbols called **operators**.

---

## 🔹 List of Arithmetic Operators

| Operator | Description         | Example (`a = 10`, `b = 3`) | Result     |
| -------- | ------------------- | --------------------------- | ---------- |
| `+`      | Addition            | `a + b`                     | `13`       |
| `-`      | Subtraction         | `a - b`                     | `7`        |
| `*`      | Multiplication      | `a * b`                     | `30`       |
| `/`      | Division (float)    | `a / b`                     | `3.333...` |
| `//`     | Floor Division      | `a // b`                    | `3`        |
| `%`      | Modulus (Remainder) | `a % b`                     | `1`        |
| `**`     | Exponentiation      | `a ** b`                    | `1000`     |

---

## ✅ Examples

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3 (whole number division)
print(a % b)   # 1 (remainder)
print(a ** b)  # 1000 (10 to the power of 3)
```

---

## 🔍 Note on Division

* `/` always returns a `float`, even if the result is a whole number:

  ```python
  print(6 / 2)   # 3.0
  ```
* `//` returns an `int` if both operands are `int`, or `float` if any operand is `float`.

---

## 🧠 Combine with `input()` Example

```python
x = int(input("Enter a number: "))
y = int(input("Enter another number: "))

print(f"Sum = {x + y}")
print(f"Product = {x * y}")
print(f"Power = {x ** y}")
```
---

## 12. Comparison Operators

**Comparison operators** are used to compare two values and return a **Boolean result**: `True` or `False`.

---

## 🔹 List of Comparison Operators

| Operator | Description              | Example (`a = 5`, `b = 3`) | Result  |
| -------- | ------------------------ | -------------------------- | ------- |
| `==`     | Equal to                 | `a == b`                   | `False` |
| `!=`     | Not equal to             | `a != b`                   | `True`  |
| `>`      | Greater than             | `a > b`                    | `True`  |
| `<`      | Less than                | `a < b`                    | `False` |
| `>=`     | Greater than or equal to | `a >= b`                   | `True`  |
| `<=`     | Less than or equal to    | `a <= b`                   | `False` |

---

## ✅ Examples

```python
a = 5
b = 3

print(a == b)   # False
print(a != b)   # True
print(a > b)    # True
print(a < b)    # False
print(a >= b)   # True
print(a <= b)   # False
```

---

## 🔄 Used in Conditions

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

---

## 🧠 Works with Other Data Types Too

```python
print("apple" == "Apple")  # False (case-sensitive)
print(3.0 == 3)            # True
print(True != False)       # True
```

---

## 13. Logical Operators

**Logical operators** are used to combine multiple **conditions (Boolean expressions)** and return `True` or `False`.

---

## 🔹 Logical Operators List

| Operator | Description                             | Example            | Result     |
| -------- | --------------------------------------- | ------------------ | ---------- |
| `and`    | True if **both** conditions are True    | `x > 5 and x < 10` | True/False |
| `or`     | True if **at least one** is True        | `x < 0 or x > 100` | True/False |
| `not`    | Inverts the result (True → False, etc.) | `not(x > 5)`       | True/False |

---

## ✅ Examples

```python
x = 7

print(x > 5 and x < 10)   # True
print(x < 5 or x > 10)    # False
print(not(x == 7))        # False
```

---

## 🧠 Used in Conditions

```python
age = int(input("Enter your age: "))
has_id = input("Do you have ID? (yes/no): ").lower() == "yes"

if age >= 18 and has_id:
    print("Access granted.")
else:
    print("Access denied.")
```

---

## 🔍 Truth Table (for `and` / `or`)

### `and`

| A     | B     | A and B |
| ----- | ----- | ------- |
| True  | True  | True    |
| True  | False | False   |
| False | True  | False   |
| False | False | False   |

### `or`

| A     | B     | A or B |
| ----- | ----- | ------ |
| True  | True  | True   |
| True  | False | True   |
| False | True  | True   |
| False | False | False  |

---

## 14. Membership Operators

**Membership operators** are used to test whether a **value exists** in a **sequence** (like a string, list, tuple, or set).

---

## 🔹 Operators

| Operator | Description                        | Example              | Result |
| -------- | ---------------------------------- | -------------------- | ------ |
| `in`     | Returns `True` if value is present | `"a" in "apple"`     | `True` |
| `not in` | Returns `True` if value is absent  | `"x" not in "apple"` | `True` |

---

## ✅ Examples with Strings

```python
word = "Python"

print("P" in word)       # True
print("y" in word)       # True
print("z" in word)       # False
print("on" in word)      # True (checks substring)
```

---

## ✅ Examples with Lists

```python
fruits = ["apple", "banana", "cherry"]

print("apple" in fruits)       # True
print("grape" not in fruits)   # True
```

---

## ✅ Examples with Tuples & Sets

```python
nums = (1, 2, 3)
print(2 in nums)  # True

unique = {10, 20, 30}
print(40 not in unique)  # True
```

---

## 🔍 Use in `if` Statements

```python
colors = ["red", "green", "blue"]
color = input("Enter a color: ").lower()

if color in colors:
    print("Color is available!")
else:
    print("Color not found.")
```
---

## 15. Identity Operators

**Identity operators** are used to compare the **memory location** of two objects — whether they are actually the **same object**, not just equal in value.

---

## 🔹 Operators

| Operator | Description                                                   | Example      | Result       |
| -------- | ------------------------------------------------------------- | ------------ | ------------ |
| `is`     | Returns `True` if both variables **point to the same object** | `x is y`     | `True/False` |
| `is not` | Returns `True` if they **do not point to the same object**    | `x is not y` | `True/False` |

---

## ✅ Examples

```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a == b)     # True (same values)
print(a is b)     # True (same object)

print(a == c)     # True (same values)
print(a is c)     # False (different objects)
```

---

## 🧠 Why It Matters

* `==` → checks **value equality**
* `is` → checks **object identity** (same memory address)

---

## 🔍 Example with `None`

```python
x = None

if x is None:
    print("x is None")        # ✅ Recommended way
```

> Avoid writing `x == None`; use `x is None` for checking `None` identity.

---

## 💡 Use Case

```python
x = 5
y = 5
print(x is y)   # True (small integers are cached in Python)
```

> But this may not hold true for larger or more complex objects.

---
