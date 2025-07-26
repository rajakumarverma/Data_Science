### 🔹 Data Types in Python

Python has several **built-in data types** used to store different kinds of values. Here's an overview:

---

## 📦 1. **Basic Data Types**

| Type    | Example         | Description                      |
| ------- | --------------- | -------------------------------- |
| `int`   | `10`, `-5`      | Integer numbers                  |
| `float` | `3.14`, `-0.01` | Decimal (floating-point) numbers |
| `str`   | `'Hello'`       | Text (string)                    |
| `bool`  | `True`, `False` | Boolean values (True or False)   |

```python
a = 10        # int
b = 3.14      # float
c = "Python"  # str
d = True      # bool
```

---

## 📚 2. **Collection Data Types**

| Type    | Example                        | Description                      |
| ------- | ------------------------------ | -------------------------------- |
| `list`  | `[1, 2, 3]`                    | Ordered, changeable collection   |
| `tuple` | `(1, 2, 3)`                    | Ordered, unchangeable collection |
| `set`   | `{1, 2, 3}`                    | Unordered, no duplicates         |
| `dict`  | `{"name": "Alice", "age": 25}` | Key-value pairs                  |

```python
my_list = [1, 2, 3]                 # list
my_tuple = (1, 2, 3)                # tuple
my_set = {1, 2, 3}                  # set
my_dict = {"name": "Alice", "age": 25}  # dict
```

---

## 🔧 3. **Special Types**

| Type       | Example  | Description                             |
| ---------- | -------- | --------------------------------------- |
| `NoneType` | `None`   | Represents the absence of a value       |
| `complex`  | `3 + 4j` | Complex numbers (used in advanced math) |

```python
x = None       # NoneType
z = 3 + 4j     # complex
```

---

## 🧪 4. **Type Checking**

Use the `type()` function to check the data type:

```python
x = 42
print(type(x))   # <class 'int'>
```
