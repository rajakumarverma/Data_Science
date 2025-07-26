### ⚠️ `raise` Statement in Python

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

