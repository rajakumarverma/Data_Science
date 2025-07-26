### 🔗 Logical Operators in Python

**Logical operators** are used to combine multiple **conditions (Boolean expressions)** and return `True` or `False`.

---

## 🔹 Logical Operators List

| Operator | Description                             | Example            | Result     |
| -------- | --------------------------------------- | ------------------ | ---------- |
| `and`    | True if **both** conditions are True    | `x > 5 and x < 10` | True/False |
| `or`     | True if **at least one** is True        | `x < 0 or x > 100` | True/False |
| `not`    | Inverts the result (True → False, etc.) | `not(x > 5)`       | True/False |

---

## ✅ Examples

```python
x = 7

print(x > 5 and x < 10)   # True
print(x < 5 or x > 10)    # False
print(not(x == 7))        # False
```

---

## 🧠 Used in Conditions

```python
age = int(input("Enter your age: "))
has_id = input("Do you have ID? (yes/no): ").lower() == "yes"

if age >= 18 and has_id:
    print("Access granted.")
else:
    print("Access denied.")
```

---

## 🔍 Truth Table (for `and` / `or`)

### `and`

| A     | B     | A and B |
| ----- | ----- | ------- |
| True  | True  | True    |
| True  | False | False   |
| False | True  | False   |
| False | False | False   |

### `or`

| A     | B     | A or B |
| ----- | ----- | ------ |
| True  | True  | True   |
| True  | False | True   |
| False | True  | True   |
| False | False | False  |

