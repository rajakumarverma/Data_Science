### 📂 File Reading in Python (`'r'` mode)

The `'r'` mode is used to **read data from a file** in Python.
This is the **default** mode when opening a file.

---

## 🔹 Basic Syntax

```python
file = open("filename.txt", "r")
# or simply:
file = open("filename.txt")

# Read file content
content = file.read()

# Always close the file
file.close()
```

---

## ✅ Example

```python
file = open("example.txt", "r")

print(file.read())

file.close()
```

---

## 🔹 Best Practice: `with` Statement

Automatically handles file closing:

```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```

---

## 🔹 Reading Methods

| Method        | Description                           |
| ------------- | ------------------------------------- |
| `read()`      | Reads the **entire file** as a string |
| `readline()`  | Reads **one line** at a time          |
| `readlines()` | Reads **all lines** into a list       |

### Example:

```python
with open("example.txt", "r") as f:
    print(f.readline())   # Reads first line
    print(f.readlines())  # Reads remaining lines as list
```

---

## 🔹 Looping Through Lines

```python
with open("example.txt", "r") as f:
    for line in f:
        print(line.strip())  # strip() removes \n
```

---

## 🔍 What if File Doesn't Exist?

Opening a non-existent file in `'r'` mode causes an error:

```python
with open("missing.txt", "r") as f:
    # FileNotFoundError
```

Handle with `try` block:

```python
try:
    with open("missing.txt", "r") as f:
        print(f.read())
except FileNotFoundError:
    print("File not found!")
```
