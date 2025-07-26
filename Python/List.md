### 📋 List in Python

A **list** is a built-in data type in Python used to store **a collection of items**.
Lists are **ordered**, **mutable** (can be changed), and can contain **mixed data types**.

---

## 🔹 Creating a List

```python
my_list = [1, 2, 3, 4]
names = ["Alice", "Bob", "Charlie"]
mixed = [1, "two", 3.0, True]
empty = []
```

---

## 🔹 Accessing List Elements (Indexing)

```python
fruits = ["apple", "banana", "cherry"]

print(fruits[0])    # 'apple'
print(fruits[-1])   # 'cherry'
```

---

## 🔹 Slicing a List

```python
print(fruits[0:2])  # ['apple', 'banana']
print(fruits[:])    # ['apple', 'banana', 'cherry']
```

---

## 🔹 Modifying List Elements

```python
fruits[1] = "blueberry"
print(fruits)  # ['apple', 'blueberry', 'cherry']
```

---

## 🔹 List Methods

| Method         | Description                           |
| -------------- | ------------------------------------- |
| `append(x)`    | Adds `x` to the end                   |
| `insert(i, x)` | Inserts `x` at index `i`              |
| `remove(x)`    | Removes first occurrence of `x`       |
| `pop([i])`     | Removes and returns item at index `i` |
| `sort()`       | Sorts the list in ascending order     |
| `reverse()`    | Reverses the list                     |
| `clear()`      | Removes all items                     |
| `index(x)`     | Returns index of first `x`            |
| `count(x)`     | Counts how many times `x` appears     |

---

### ✅ Example: Common Operations

```python
numbers = [3, 1, 4, 1, 5]

numbers.append(9)         # [3, 1, 4, 1, 5, 9]
numbers.insert(1, 10)     # [3, 10, 1, 4, 1, 5, 9]
numbers.remove(1)         # [3, 10, 4, 1, 5, 9] (removes first 1)
numbers.sort()            # [1, 3, 4, 5, 9, 10]
numbers.reverse()         # [10, 9, 5, 4, 3, 1]
```

---

## 🔄 Looping Through a List

```python
for fruit in fruits:
    print(fruit)
```

---

## 🔎 Check Membership

```python
if "apple" in fruits:
    print("Apple is in the list")
```
