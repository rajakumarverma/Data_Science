### 📦 Tuple in Python

A **tuple** is a collection data type in Python that is:

* **Ordered**
* **Immutable** (cannot be changed after creation)
* Allows **duplicates**
* Can store **mixed data types**

---

## 🔹 Creating a Tuple

```python
my_tuple = (1, 2, 3)
names = ("Alice", "Bob", "Charlie")
mixed = (1, "two", 3.0, True)
single = (5,)      # Note the comma – needed for single-item tuple
empty = ()         # Empty tuple
```

---

## 🔹 Accessing Tuple Elements

```python
print(my_tuple[0])     # 1
print(my_tuple[-1])    # 3
```

---

## 🔹 Tuple Slicing

```python
print(my_tuple[1:])    # (2, 3)
print(my_tuple[:2])    # (1, 2)
```

---

## 🔒 Tuples Are Immutable

You **cannot modify**, **append**, or **remove** elements:

```python
# my_tuple[0] = 10   ❌ TypeError
# my_tuple.append(4) ❌ AttributeError
```

But you can **reassign** the entire tuple:

```python
my_tuple = (4, 5, 6)
```

---

## 🔁 Looping Through a Tuple

```python
for item in my_tuple:
    print(item)
```

---

## 🔹 Tuple Methods

Tuples have **limited methods**:

| Method     | Description                       |
| ---------- | --------------------------------- |
| `count(x)` | Counts how many times `x` appears |
| `index(x)` | Returns the index of first `x`    |

```python
nums = (1, 2, 2, 3)
print(nums.count(2))  # 2
print(nums.index(3))  # 3
```

---

## 🔁 Tuple Packing & Unpacking

```python
# Packing
person = ("Alice", 25, "Engineer")

# Unpacking
name, age, job = person
print(name)  # Alice
print(age)   # 25
```

---

## 🆚 Tuple vs List

| Feature     | List (`[]`)     | Tuple (`()`)    |
| ----------- | --------------- | --------------- |
| Mutable     | ✅ Yes           | ❌ No            |
| Syntax      | `[1, 2, 3]`     | `(1, 2, 3)`     |
| Methods     | Many            | Few             |
| Use case    | Changing data   | Fixed data      |
| Performance | Slightly slower | Slightly faster |
