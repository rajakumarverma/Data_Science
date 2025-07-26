### 🔁 Iterators in Python

An **iterator** is any object in Python that **can be iterated (looped) over**, one element at a time.
It uses two main methods:

* `__iter__()` → returns the iterator object itself
* `__next__()` → returns the **next value** from the iterator

---

## ✅ What is Iterable vs Iterator?

| Term         | Description                               | Examples                                  |
| ------------ | ----------------------------------------- | ----------------------------------------- |
| **Iterable** | An object you can loop over               | `list`, `tuple`, `str`, `set`, etc.       |
| **Iterator** | An object that **remembers its position** | Result of calling `iter()` on an iterable |

---

## 🔹 Example: Creating an Iterator

```python
nums = [1, 2, 3]
it = iter(nums)

print(next(it))  # 1
print(next(it))  # 2
print(next(it))  # 3
```

---

## 🔹 Looping with an Iterator

```python
nums = [10, 20, 30]
it = iter(nums)

for num in it:
    print(num)
```

---

## 🔹 Custom Iterator Class

```python
class Counter:
    def __init__(self, max):
        self.max = max
        self.current = 1

    def __iter__(self):
        return self

    def __next__(self):
        if self.current <= self.max:
            val = self.current
            self.current += 1
            return val
        else:
            raise StopIteration

c = Counter(3)
for num in c:
    print(num)
```

**Output:**

```
1
2
3
```

---

## 🔹 Summary

| Concept          | Explanation                          |
| ---------------- | ------------------------------------ |
| `iter(obj)`      | Gets iterator from iterable          |
| `next(iterator)` | Gets next item                       |
| `StopIteration`  | Raised when there are no more items  |
| Custom Iterator  | Define `__iter__()` and `__next__()` |

