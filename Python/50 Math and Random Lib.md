### 🔢 `math` and `random` Libraries in Python

Python provides built-in libraries to handle **mathematical operations** and **randomization**:

---

## 📐 `math` Module (Mathematical Functions)

### ✅ Importing:

```python
import math
```

### 🔹 Common `math` Functions:

| Function            | Description                  | Example                     |
| ------------------- | ---------------------------- | --------------------------- |
| `math.sqrt(x)`      | Square root                  | `math.sqrt(16)` → `4.0`     |
| `math.pow(x, y)`    | Power (x^y)                  | `math.pow(2, 3)` → `8.0`    |
| `math.factorial(n)` | Factorial                    | `math.factorial(5)` → `120` |
| `math.floor(x)`     | Round **down**               | `math.floor(3.9)` → `3`     |
| `math.ceil(x)`      | Round **up**                 | `math.ceil(3.1)` → `4`      |
| `math.pi`           | π (3.14159...)               | `math.pi`                   |
| `math.e`            | Euler’s number (2.718...)    | `math.e`                    |
| `math.log(x, base)` | Logarithm (default base `e`) | `math.log(100, 10)` → `2`   |

---

## 🎲 `random` Module (Randomization)

### ✅ Importing:

```python
import random
```

### 🔹 Common `random` Functions:

| Function                | Description                        | Example                        |
| ----------------------- | ---------------------------------- | ------------------------------ |
| `random.random()`       | Random float between 0 and 1       | `0.7481...`                    |
| `random.randint(a, b)`  | Random int in range \[a, b]        | `random.randint(1, 6)`         |
| `random.choice(seq)`    | Random item from list/tuple/string | `random.choice(['a','b','c'])` |
| `random.shuffle(list)`  | Shuffle the list in-place          |                                |
| `random.uniform(a, b)`  | Random float between a and b       | `random.uniform(1, 5)`         |
| `random.sample(pop, k)` | Get `k` unique random elements     | `random.sample(range(10), 3)`  |

---

## ✅ Examples

### 1. Roll a Dice

```python
import random
print(random.randint(1, 6))
```

### 2. Shuffle a List

```python
items = [1, 2, 3, 4, 5]
random.shuffle(items)
print(items)
```

### 3. Calculate Circle Area

```python
import math
radius = 5
area = math.pi * math.pow(radius, 2)
print(area)
```

---

## 🧠 Summary

| Library  | Use For                          |
| -------- | -------------------------------- |
| `math`   | Advanced mathematical operations |
| `random` | Simulations, games, sampling     |

