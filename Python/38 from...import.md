### 📦 `from ... import` in Python

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

