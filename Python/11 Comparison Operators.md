### 🔍 Comparison Operators in Python

**Comparison operators** are used to compare two values and return a **Boolean result**: `True` or `False`.

---

## 🔹 List of Comparison Operators

| Operator | Description              | Example (`a = 5`, `b = 3`) | Result  |
| -------- | ------------------------ | -------------------------- | ------- |
| `==`     | Equal to                 | `a == b`                   | `False` |
| `!=`     | Not equal to             | `a != b`                   | `True`  |
| `>`      | Greater than             | `a > b`                    | `True`  |
| `<`      | Less than                | `a < b`                    | `False` |
| `>=`     | Greater than or equal to | `a >= b`                   | `True`  |
| `<=`     | Less than or equal to    | `a <= b`                   | `False` |

---

## ✅ Examples

```python
a = 5
b = 3

print(a == b)   # False
print(a != b)   # True
print(a > b)    # True
print(a < b)    # False
print(a >= b)   # True
print(a <= b)   # False
```

---

## 🔄 Used in Conditions

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

---

## 🧠 Works with Other Data Types Too

```python
print("apple" == "Apple")  # False (case-sensitive)
print(3.0 == 3)            # True
print(True != False)       # True
```
