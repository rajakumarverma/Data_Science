### Variable Assignment in Python

In Python, **variables** are used to store data. **Variable assignment** means assigning a value to a variable name so it can be used later in your code.

---

### 🔹 Basic Syntax

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

---

### 🔹 Rules for Naming Variables

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

---

### 🔹 Multiple Assignments

Python allows multiple assignments in one line:

```python
a, b, c = 1, 2, 3
```

All assigned to the same value:

```python
x = y = z = 0
```

---

### 🔹 Swapping Variables

Python lets you swap variables without a temporary variable:

```python
a = 5
b = 10
a, b = b, a
```

---

### 🔹 Dynamic Typing

Python is dynamically typed, so you don't declare types explicitly:

```python
x = 10       # x is an int
x = "Hello"  # now x is a str
```
