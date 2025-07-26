### 📝 File Writing in Python (`'w'` mode)

The `'w'` mode is used to **write data to a file**.
It **creates** the file if it doesn't exist, and **overwrites** it if it does.

---

## 🔹 Basic Syntax

```python
file = open("filename.txt", "w")
file.write("Hello, world!")
file.close()
```

---

## ✅ Example

```python
with open("output.txt", "w") as f:
    f.write("This is line 1.\n")
    f.write("This is line 2.\n")
```

📁 This will create or overwrite `output.txt` with:

```
This is line 1.
This is line 2.
```

---

## ⚠️ Overwriting Behavior

```python
with open("data.txt", "w") as f:
    f.write("First write.\n")

# Opening in 'w' mode again overwrites it:
with open("data.txt", "w") as f:
    f.write("This will erase previous content.")
```

---

## 🔹 Writing Multiple Lines

You can use `.writelines()` with a list of strings:

```python
lines = ["Line A\n", "Line B\n", "Line C\n"]
with open("list_output.txt", "w") as f:
    f.writelines(lines)
```

---

## 🧠 Reminder

Always use `\n` for line breaks — Python doesn't add them automatically.

---

## 🔄 Summary: File Modes

| Mode  | Action                        |
| ----- | ----------------------------- |
| `'r'` | Read (file must exist)        |
| `'w'` | Write (creates or overwrites) |
| `'a'` | Append (adds to end of file)  |
| `'x'` | Create (fails if file exists) |

