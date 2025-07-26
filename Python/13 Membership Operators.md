### 🧭 Membership Operators in Python

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
