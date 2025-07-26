### 🔁 `for` Loop in Python

A `for` loop in Python is used to **iterate over a sequence** (like a list, string, tuple, or range) and execute a block of code for each item.

---

## 🔹 Basic Syntax

```python
for variable in sequence:
    # code block
```

---

## ✅ Example with `range()`

```python
for i in range(5):
    print(i)
```

**Output:**

```
0
1
2
3
4
```

> `range(5)` generates numbers from `0` to `4` (not including `5`)

---

## 🔹 `range(start, stop, step)`

```python
for i in range(1, 10, 2):
    print(i)
```

**Output:**
`1 3 5 7 9`

---

## 🔹 Looping Through a List

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

---

## 🔹 Looping Through a String

```python
for char in "Python":
    print(char)
```

---

## 🔹 `for` with `else` (Optional)

```python
for i in range(3):
    print(i)
else:
    print("Loop completed")
```

> The `else` block runs **only if the loop finishes without `break`**.

---

## 🔹 Using `break` and `continue`

```python
for i in range(5):
    if i == 3:
        break   # exits the loop
    print(i)

for i in range(5):
    if i == 2:
        continue  # skips this iteration
    print(i)
```
