### 📖 Dictionary in Python

A **dictionary** is a built-in Python data type used to store **key–value pairs**.
It is:

* ✅ **Unordered** (as of Python 3.6+, insertion order is preserved)
* ✅ **Mutable** (you can change it)
* ✅ **Indexed by keys, not positions**
* ❌ Keys must be **unique** and **immutable** (strings, numbers, tuples)

---

## 🔹 Creating a Dictionary

```python
person = {
    "name": "Alice",
    "age": 25,
    "is_student": True
}
```

Or using the `dict()` constructor:

```python
person = dict(name="Bob", age=30)
```

---

## 🔹 Accessing Values

```python
print(person["name"])        # Alice
print(person.get("age"))     # 25
print(person.get("email"))   # None (safe way to access)
```

---

## 🔹 Adding / Updating Items

```python
person["email"] = "alice@example.com"  # Add
person["age"] = 26                     # Update
```

---

## 🔹 Removing Items

```python
person.pop("age")         # Removes 'age'
del person["is_student"]  # Removes 'is_student'
person.clear()            # Clears the entire dictionary
```

---

## 🔹 Looping Through a Dictionary

```python
for key in person:
    print(key, person[key])

# Or:
for key, value in person.items():
    print(key, value)
```

---

## 🔹 Dictionary Methods

| Method          | Description                              |
| --------------- | ---------------------------------------- |
| `get(key)`      | Returns value or `None` if key not found |
| `keys()`        | Returns a view of all keys               |
| `values()`      | Returns a view of all values             |
| `items()`       | Returns a view of key–value pairs        |
| `update(dict2)` | Merges `dict2` into current dictionary   |
| `pop(key)`      | Removes key and returns its value        |
| `clear()`       | Empties the dictionary                   |

---

## ✅ Example

```python
student = {
    "name": "John",
    "marks": 85,
    "passed": True
}

print(student["marks"])          # 85
student["marks"] += 5            # Update
print(student.get("age", "N/A")) # N/A
```

---

## 🧠 Nested Dictionary

```python
users = {
    "user1": {"name": "Alice", "age": 25},
    "user2": {"name": "Bob", "age": 30}
}

print(users["user1"]["name"])  # Alice
```
