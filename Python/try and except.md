### 🛡️ `try` / `except` in Python

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

