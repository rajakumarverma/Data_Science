### 📘 Dictionary Comprehension in Python

**Dictionary comprehension** allows you to create a new dictionary by writing **key-value pairs in a single line**, similar to list comprehension.

---

## 🔹 Basic Syntax

```python
{key: value for item in iterable}
```

### ✅ With Condition:

```python
{key: value for item in iterable if condition}
```

---

## ✅ Example 1: Squares Dictionary

```python
squares = {x: x**2 for x in range(5)}
print(squares)  # {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

---

## ✅ Example 2: Convert Two Lists to Dict

```python
keys = ['a', 'b', 'c']
values = [1, 2, 3]

combined = {k: v for k, v in zip(keys, values)}
print(combined)  # {'a': 1, 'b': 2, 'c': 3}
```

---

## ✅ Example 3: Filter Items in a Dict

```python
original = {'apple': 10, 'banana': 3, 'cherry': 15}
filtered = {k: v for k, v in original.items() if v > 5}
print(filtered)  # {'apple': 10, 'cherry': 15}
```

---

## ✅ Example 4: Swap Keys and Values

```python
data = {'a': 1, 'b': 2}
swapped = {v: k for k, v in data.items()}
print(swapped)  # {1: 'a', 2: 'b'}
```

---

## ✅ Example 5: Add Condition with If/Else

```python
nums = range(5)
labels = {x: ("even" if x % 2 == 0 else "odd") for x in nums}
print(labels)  # {0: 'even', 1: 'odd', 2: 'even', 3: 'odd', 4: 'even'}
```

---

## 🧠 Summary

| Feature              | Benefit                          |
| -------------------- | -------------------------------- |
| One-line dicts       | Clean, readable code             |
| Filters & transforms | Easily filter or modify items    |
| Fast and Pythonic    | Better performance in many cases |

