### ➗ Arithmetic Operators in Python

Python supports all basic **arithmetic operations** using special symbols called **operators**.

---

## 🔹 List of Arithmetic Operators

| Operator | Description         | Example (`a = 10`, `b = 3`) | Result     |
| -------- | ------------------- | --------------------------- | ---------- |
| `+`      | Addition            | `a + b`                     | `13`       |
| `-`      | Subtraction         | `a - b`                     | `7`        |
| `*`      | Multiplication      | `a * b`                     | `30`       |
| `/`      | Division (float)    | `a / b`                     | `3.333...` |
| `//`     | Floor Division      | `a // b`                    | `3`        |
| `%`      | Modulus (Remainder) | `a % b`                     | `1`        |
| `**`     | Exponentiation      | `a ** b`                    | `1000`     |

---

## ✅ Examples

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3 (whole number division)
print(a % b)   # 1 (remainder)
print(a ** b)  # 1000 (10 to the power of 3)
```

---

## 🔍 Note on Division

* `/` always returns a `float`, even if the result is a whole number:

  ```python
  print(6 / 2)   # 3.0
  ```
* `//` returns an `int` if both operands are `int`, or `float` if any operand is `float`.

---

## 🧠 Combine with `input()` Example

```python
x = int(input("Enter a number: "))
y = int(input("Enter another number: "))

print(f"Sum = {x + y}")
print(f"Product = {x * y}")
print(f"Power = {x ** y}")
```
