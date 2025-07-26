### 🔁 Type Casting in Python (Type Conversion)

**Type casting** means converting one data type into another. Python provides **built-in functions** for this.

---

## 🔹 Common Type Casting Functions

| Function   | Converts To | Example                           |
| ---------- | ----------- | --------------------------------- |
| `int(x)`   | Integer     | `int("5")` → `5`                  |
| `float(x)` | Float       | `float("3.14")` → `3.14`          |
| `str(x)`   | String      | `str(100)` → `"100"`              |
| `bool(x)`  | Boolean     | `bool("")` → `False`              |
| `list(x)`  | List        | `list("abc")` → `['a', 'b', 'c']` |
| `tuple(x)` | Tuple       | `tuple([1, 2])` → `(1, 2)`        |
| `set(x)`   | Set         | `set([1, 2, 2])` → `{1, 2}`       |

---

## ✅ Examples

```python
# To integer
print(int("10"))       # 10
print(int(3.99))        # 3 (decimal part removed)

# To float
print(float("4.5"))    # 4.5
print(float(2))        # 2.0

# To string
print(str(123))        # '123'
print(str(True))       # 'True'

# To boolean
print(bool(""))        # False
print(bool("hello"))   # True
print(bool(0))         # False
print(bool(1))         # True

# To list
print(list("abc"))     # ['a', 'b', 'c']
print(list((1, 2)))    # [1, 2]
```

---

## ⚠️ Things to Watch Out For

1. **Invalid conversions raise errors:**

   ```python
   int("abc")     # ValueError
   float("hello") # ValueError
   ```

2. **`bool()` follows these rules:**

   * `False`: `0`, `0.0`, `''`, `[]`, `{}`, `None`
   * `True`: everything else
