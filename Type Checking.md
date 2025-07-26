### 🔎 Type Checking in Python

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

