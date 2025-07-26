### 🕒 Date & Time in Python

Python’s built-in `datetime` module makes it easy to **work with dates and times** — getting the current time, formatting dates, doing arithmetic, and more.

---

## 🔹 Import the Module

```python
import datetime
```

---

## ✅ Get Current Date and Time

```python
from datetime import datetime

now = datetime.now()
print("Now:", now)
print("Date:", now.date())
print("Time:", now.time())
```

---

## ✅ Format Dates (`strftime()`)

```python
from datetime import datetime

now = datetime.now()
formatted = now.strftime("%Y-%m-%d %H:%M:%S")
print(formatted)  # e.g. 2025-07-26 14:30:45
```

### 📌 Common Format Codes:

| Code | Meaning         | Example |
| ---- | --------------- | ------- |
| `%Y` | Year (4 digits) | 2025    |
| `%m` | Month (01–12)   | 07      |
| `%d` | Day (01–31)     | 26      |
| `%H` | Hour (00–23)    | 14      |
| `%M` | Minute (00–59)  | 30      |
| `%S` | Second (00–59)  | 45      |

---

## ✅ Parse String to Date (`strptime()`)

```python
from datetime import datetime

date_str = "2025-07-26"
date_obj = datetime.strptime(date_str, "%Y-%m-%d")
print(date_obj)  # 2025-07-26 00:00:00
```

---

## ✅ Get Today's Date

```python
from datetime import date

today = date.today()
print(today)
```

---

## ✅ Date Arithmetic

```python
from datetime import timedelta, date

today = date.today()
future = today + timedelta(days=10)
past = today - timedelta(days=5)

print("10 days from now:", future)
print("5 days ago:", past)
```

---

## ✅ Get Individual Components

```python
now = datetime.now()

print(now.year)   # 2025
print(now.month)  # 7
print(now.day)    # 26
```

---

## 🧠 Summary

| Task              | Tool             |
| ----------------- | ---------------- |
| Current date/time | `datetime.now()` |
| Format date/time  | `strftime()`     |
| Parse from string | `strptime()`     |
| Add/Subtract days | `timedelta()`    |
| Just date         | `date.today()`   |

