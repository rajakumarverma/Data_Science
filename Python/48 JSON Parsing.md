### 🔄 JSON Parsing in Python

**JSON (JavaScript Object Notation)** is a common format for **data exchange** (e.g., APIs, config files).
Python’s built-in `json` module lets you **parse** JSON into Python objects and **convert** Python objects to JSON.

---

## 🔹 Step 1: Import the `json` Module

```python
import json
```

---

## ✅ Parsing JSON → Python (`json.loads()`)

```python
import json

json_data = '{"name": "Alice", "age": 25, "city": "New York"}'
python_dict = json.loads(json_data)

print(python_dict)
print(python_dict['name'])  # Output: Alice
```

> 🔸 `json.loads()` converts a **JSON string** to a **Python dictionary**.

---

## ✅ Converting Python → JSON (`json.dumps()`)

```python
data = {"name": "Bob", "age": 30, "active": True}
json_string = json.dumps(data)

print(json_string)
```

> 🔸 `json.dumps()` converts a **Python object** to a **JSON string**.

---

## ✅ Reading JSON from a File (`json.load()`)

```python
with open('data.json', 'r') as file:
    data = json.load(file)

print(data)
```

> 🔸 `json.load()` reads and parses JSON **from a file**.

---

## ✅ Writing JSON to a File (`json.dump()`)

```python
info = {"product": "Laptop", "price": 799}

with open('output.json', 'w') as file:
    json.dump(info, file)
```

> 🔸 `json.dump()` writes JSON **to a file**.

---

## 🔹 Common Python ↔ JSON Type Mapping

| Python           | JSON         |
| ---------------- | ------------ |
| `dict`           | object       |
| `list`           | array        |
| `str`            | string       |
| `int`, `float`   | number       |
| `True` / `False` | true / false |
| `None`           | null         |

---

## 🧠 Extra: Pretty Print JSON

```python
print(json.dumps(data, indent=4))
```

