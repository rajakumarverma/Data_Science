### 🧠 List Comprehension in Python

**List comprehension** is a concise way to create lists using a **single line of code**.
It's faster and cleaner than using a traditional `for` loop.

---

## 🔹 Basic Syntax

```python
[expression for item in iterable]
```

### ✅ With Condition:

```python
[expression for item in iterable if condition]
```

---

## ✅ Example 1: Squares of Numbers

```python
squares = [x**2 for x in range(5)]
print(squares)  # Output: [0, 1, 4, 9, 16]
```

---

## ✅ Example 2: Filter Even Numbers

```python
evens = [x for x in range(10) if x % 2 == 0]
print(evens)  # Output: [0, 2, 4, 6, 8]
```

---

## ✅ Example 3: Convert to Uppercase

```python
words = ["apple", "banana", "cherry"]
uppercased = [word.upper() for word in words]
print(uppercased)  # ['APPLE', 'BANANA', 'CHERRY']
```

---

## ✅ Example 4: Nested Loops (2D Comprehension)

```python
pairs = [(x, y) for x in [1, 2] for y in [3, 4]]
print(pairs)  # [(1, 3), (1, 4), (2, 3), (2, 4)]
```

---

## ✅ Example 5: If/Else Inside List Comprehension

```python
labels = ["even" if x % 2 == 0 else "odd" for x in range(5)]
print(labels)  # ['even', 'odd', 'even', 'odd', 'even']
```

---

## 🧠 Benefits

* More **concise** and **readable**
* Often **faster** than using loops
* Great for filtering, transforming, or flattening lists

