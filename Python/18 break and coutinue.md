### ⛔ `break` and 🔁 `continue` in Python

These are **loop control statements** used to change the normal flow of `for` or `while` loops.

---

## 🔹 `break` Statement

* **Immediately exits** the loop.
* The loop stops even if the condition is still `True`.

### ✅ Example:

```python
for i in range(5):
    if i == 3:
        break
    print(i)
```

**Output:**

```
0
1
2
```

---

## 🔹 `continue` Statement

* **Skips the current iteration** and goes to the **next one**.
* The loop **continues**, but skips the rest of the code **only for that iteration**.

### ✅ Example:

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

**Output:**

```
0
1
3
4
```

---

## 🔄 With `while` Loop

```python
x = 0
while x < 5:
    x += 1
    if x == 3:
        continue
    if x == 5:
        break
    print(x)
```

**Output:**

```
1
2
4
```

---

## 🧠 Use Case: Skip or Exit Based on User Input

```python
while True:
    name = input("Enter your name (or type 'exit'): ")
    if name == "exit":
        break
    if name == "":
        continue
    print("Hello", name)
```
