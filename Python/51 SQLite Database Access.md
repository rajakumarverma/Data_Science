### 🗃️ SQLite Database Access in Python

SQLite is a **lightweight, built-in SQL database** in Python — perfect for small projects or prototyping.

Python provides the `sqlite3` module to **connect**, **create tables**, **insert data**, and **run queries**.

---

## 🔹 Step 1: Import & Connect

```python
import sqlite3

# Connect to a database (creates if not exists)
conn = sqlite3.connect('example.db')

# Create a cursor object to execute SQL
cursor = conn.cursor()
```

---

## 🔹 Step 2: Create a Table

```python
cursor.execute('''
CREATE TABLE IF NOT EXISTS users (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT,
    age INTEGER
)
''')
```

---

## 🔹 Step 3: Insert Data

```python
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Alice", 30))
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ("Bob", 25))
conn.commit()  # Save changes
```

> ✅ Always use `?` placeholders to prevent SQL injection.

---

## 🔹 Step 4: Read Data

```python
cursor.execute("SELECT * FROM users")
rows = cursor.fetchall()

for row in rows:
    print(row)
```

---

## 🔹 Step 5: Update & Delete

```python
# Update
cursor.execute("UPDATE users SET age = ? WHERE name = ?", (31, "Alice"))

# Delete
cursor.execute("DELETE FROM users WHERE name = ?", ("Bob",))

conn.commit()
```

---

## 🔹 Step 6: Close Connection

```python
conn.close()
```

---

## ✅ Example Summary

```python
import sqlite3

conn = sqlite3.connect('people.db')
cursor = conn.cursor()

cursor.execute('''CREATE TABLE IF NOT EXISTS people (id INTEGER PRIMARY KEY, name TEXT, age INTEGER)''')
cursor.execute("INSERT INTO people (name, age) VALUES (?, ?)", ("Charlie", 22))
conn.commit()

cursor.execute("SELECT * FROM people")
print(cursor.fetchall())

conn.close()
```

---

## 🔹 Optional: Convert Rows to Dictionaries

```python
conn.row_factory = sqlite3.Row
cursor = conn.cursor()

cursor.execute("SELECT * FROM users")
row = cursor.fetchone()
print(dict(row))  # {'id': 1, 'name': 'Alice', 'age': 30}
```

