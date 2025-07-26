### 🔢 `range()` Function in Python

The `range()` function is used to generate a **sequence of numbers**, commonly in `for` loops.

---

## 🔹 Syntax

```python
range(stop)
range(start, stop)
range(start, stop, step)
```

| Parameter | Description                                      |
| --------- | ------------------------------------------------ |
| `start`   | (Optional) Starting number (default is `0`)      |
| `stop`    | **(Required)** Ending number (excluded)          |
| `step`    | (Optional) Step between numbers (default is `1`) |

---

## ✅ Examples

### 1. **Basic usage with one argument**

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

---

### 2. **With start and stop**

```python
for i in range(2, 6):
    print(i)
```

**Output:**

```
2
3
4
5
```

---

### 3. **With step**

```python
for i in range(1, 10, 2):
    print(i)
```

**Output:**

```
1
3
5
7
9
```

---

### 4. **Using negative step (counting backward)**

```python
for i in range(5, 0, -1):
    print(i)
```

**Output:**

```
5
4
3
2
1
```

---

## 🔄 `range()` in Lists

You can convert a `range` to a list:

```python
nums = list(range(1, 6))
print(nums)  # [1, 2, 3, 4, 5]
```

---

## 🛑 Note

* `range()` does **not include** the stop number.
* `step` must **not be 0**, or you'll get an error.
