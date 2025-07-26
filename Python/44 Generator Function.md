### 🔄 Generator Function in Python

A **generator function** is a special type of function that **yields values one at a time**, using the `yield` keyword instead of `return`.

It **remembers its state** between calls, which makes it **memory-efficient** when working with large data or infinite sequences.

---

## 🔹 Syntax

```python
def my_generator():
    yield value1
    yield value2
    ...
```

---

## ✅ Example 1: Simple Generator

```python
def count_up_to(n):
    count = 1
    while count <= n:
        yield count
        count += 1

gen = count_up_to(3)

for num in gen:
    print(num)
```

**Output:**

```
1
2
3
```

---

## ✅ Example 2: Use `next()`

```python
def numbers():
    yield 10
    yield 20

g = numbers()
print(next(g))  # 10
print(next(g))  # 20
```

---

## ✅ Example 3: Generator Expression (like list comprehension)

```python
squares = (x**2 for x in range(5))

for s in squares:
    print(s)
```

---

## ✅ Why Use Generators?

| Feature          | Benefit                                |
| ---------------- | -------------------------------------- |
| `yield`          | Pauses function and saves state        |
| Memory-efficient | Does **not** store full list in memory |
| Lazy evaluation  | Values produced **on demand**          |
| Useful for       | Large files, streams, pipelines        |

---

## ✅ Real-World Example: Reading a File Line by Line

```python
def read_file_line_by_line(filename):
    with open(filename, 'r') as f:
        for line in f:
            yield line.strip()

for line in read_file_line_by_line('data.txt'):
    print(line)
```

---

## 🧠 Summary

* Use `yield` instead of `return` to create a generator
* Maintains state between iterations
* More efficient than returning a full list in some cases

