### 📌 Append to File in Python (`'a'` mode)

The `'a'` mode is used to **append data** to the **end of an existing file** without deleting its current content.
If the file doesn’t exist, it will be **created**.

---

## 🔹 Basic Syntax

```python
file = open("filename.txt", "a")
file.write("New content\n")
file.close()
```

---

## ✅ Example

```python
with open("log.txt", "a") as f:
    f.write("Log entry 1\n")
    f.write("Log entry 2\n")
```

Each time you run this code, it will **add** more lines at the end of `log.txt`.

---

## 🔹 Appending Multiple Lines

```python
lines = ["Line A\n", "Line B\n"]
with open("notes.txt", "a") as f:
    f.writelines(lines)
```

---

## 🧠 Tip: Always Use `\n` for New Lines

Python’s `write()` and `writelines()` won’t add line breaks automatically.
You must include `\n` at the end of each line yourself.

---

## 🔄 Compare File Modes

| Mode  | Description                   |
| ----- | ----------------------------- |
| `'r'` | Read (file must exist)        |
| `'w'` | Write (overwrites file)       |
| `'a'` | Append (adds to end of file)  |
| `'x'` | Create (fails if file exists) |

