### 🧱 Creating Modules in Python

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

