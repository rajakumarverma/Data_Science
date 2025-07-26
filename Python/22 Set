### 🔢 Set in Python

A **set** is a built-in Python data type used to store **unordered**, **unique** items.
It's useful for removing duplicates and performing **mathematical set operations** like union, intersection, etc.

---

## 🔹 Characteristics of Sets

* ✅ **Unordered** (no index)
* ✅ **Mutable** (can add/remove elements)
* ✅ **No duplicates allowed**
* ❌ **Cannot access by index**
* ✅ **Fast membership testing**

---

## 🔹 Creating a Set

```python
my_set = {1, 2, 3}
empty_set = set()  # NOT {} — that creates a dict
mixed_set = {1, "two", 3.0}
```

---

## 🔹 Duplicate Values Are Ignored

```python
s = {1, 2, 2, 3}
print(s)  # Output: {1, 2, 3}
```

---

## 🔹 Adding and Removing Elements

```python
s = {1, 2}

s.add(3)           # {1, 2, 3}
s.remove(1)        # {2, 3}
s.discard(5)       # No error if 5 not found
s.clear()          # Empty the set
```

---

## 🔹 Set Operations

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)   # Union → {1, 2, 3, 4, 5}
print(a & b)   # Intersection → {3}
print(a - b)   # Difference → {1, 2}
print(a ^ b)   # Symmetric difference → {1, 2, 4, 5}
```

---

## 🔁 Looping Through a Set

```python
for item in {"apple", "banana", "cherry"}:
    print(item)
```

> Output order is unpredictable because sets are unordered.

---

## 🔍 Membership Testing (Fast)

```python
fruits = {"apple", "banana"}
print("apple" in fruits)     # True
print("mango" not in fruits) # True
```

---

## 🆚 Set vs List vs Tuple

| Feature    | List (`[]`) | Tuple (`()`) | Set (`{}`)    |
| ---------- | ----------- | ------------ | ------------- |
| Ordered    | ✅           | ✅            | ❌             |
| Mutable    | ✅           | ❌            | ✅             |
| Duplicates | ✅ Allowed   | ✅ Allowed    | ❌ Not Allowed |
| Indexed    | ✅ Yes       | ✅ Yes        | ❌ No indexing |

