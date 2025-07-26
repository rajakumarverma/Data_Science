### 🔁 `return` Statement in Python

The `return` statement is used in a function to **send a value back** to the caller.
It also **ends** the function's execution.

---

## 🔹 Basic Syntax

```python
def function_name():
    return value
```

---

## ✅ Example 1: Return a Value

```python
def square(num):
    return num * num

result = square(4)
print(result)  # 16
```

---

## ✅ Example 2: Return Multiple Values

```python
def get_info():
    name = "Alice"
    age = 25
    return name, age

n, a = get_info()
print(n)  # Alice
print(a)  # 25
```

Returned values are packaged as a **tuple**:

```python
# Same as:
info = get_info()
print(info)  # ('Alice', 25)
```

---

## 🔹 Without a `return`

If no `return` is used, the function returns `None` by default:

```python
def say_hello():
    print("Hello")

result = say_hello()  # Prints: Hello
print(result)         # None
```

---

## 🔹 Using `return` to End a Function Early

```python
def check_even(n):
    if n % 2 == 0:
        return True
    return False
```

---

## 🧠 Summary

| Purpose of `return`     | Behavior                   |
| ----------------------- | -------------------------- |
| Return a single value   | `return x`                 |
| Return multiple values  | `return x, y, z` → tuple   |
| No return statement     | Returns `None`             |
| Ends function execution | Function stops at `return` |
