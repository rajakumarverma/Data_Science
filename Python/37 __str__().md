### 🧾 `__str__()` Method in Python

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

