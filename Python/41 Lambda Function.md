### ⚡ Lambda Function in Python

A **lambda function** is a **small, anonymous function** in Python.
It can have **any number of arguments**, but only **one expression**.

---

## 🔹 Syntax

```python
lambda arguments: expression
```

* The expression is **automatically returned**.
* Often used when a simple function is needed **temporarily or inline**.

---

## ✅ Example 1: Add two numbers

```python
add = lambda x, y: x + y
print(add(3, 5))  # Output: 8
```

---

## ✅ Example 2: Square a number

```python
square = lambda n: n * n
print(square(4))  # Output: 16
```

---

## ✅ Example 3: Use with `map()`

```python
nums = [1, 2, 3, 4]
squared = list(map(lambda x: x**2, nums))
print(squared)  # Output: [1, 4, 9, 16]
```

---

## ✅ Example 4: Use with `filter()`

```python
nums = [1, 2, 3, 4, 5]
even = list(filter(lambda x: x % 2 == 0, nums))
print(even)  # Output: [2, 4]
```

---

## ✅ Example 5: Use with `sorted()` and `key`

```python
students = [("Alice", 85), ("Bob", 92), ("Charlie", 78)]
# Sort by score
sorted_students = sorted(students, key=lambda x: x[1], reverse=True)
print(sorted_students)
```

---

## 🧠 When to Use Lambda

✅ Use for:

* One-liners
* Short throwaway functions
* Functional programming (`map`, `filter`, `reduce`)

❌ Avoid for:

* Complex logic
* Reusability (use `def` instead)

