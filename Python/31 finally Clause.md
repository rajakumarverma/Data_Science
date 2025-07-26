### 🔚 `finally` Clause in Python

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

