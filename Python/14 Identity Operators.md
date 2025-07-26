### 🆔 Identity Operators in Python

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
