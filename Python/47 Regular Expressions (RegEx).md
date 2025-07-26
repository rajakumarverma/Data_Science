### 🔍 Regular Expressions (RegEx) in Python

**Regular Expressions (RegEx)** are patterns used to **match, search, or manipulate text**.
Python provides the `re` module to work with regex.

---

## 🔹 Import the `re` Module

```python
import re
```

---

## 🔹 Common Functions

| Function       | Description                                     |
| -------------- | ----------------------------------------------- |
| `re.match()`   | Checks for a match **at the start** of a string |
| `re.search()`  | Searches for **first match** anywhere           |
| `re.findall()` | Returns **all matches** as a list               |
| `re.sub()`     | Replaces matched text                           |

---

## ✅ Basic Patterns

| Pattern  | Matches                            |
| -------- | ---------------------------------- |
| `.`      | Any character except newline       |
| `\d`     | Digit (0–9)                        |
| `\D`     | Non-digit                          |
| `\w`     | Word character (a-z, A-Z, 0–9, \_) |
| `\W`     | Non-word character                 |
| `\s`     | Whitespace                         |
| `\S`     | Non-whitespace                     |
| `^`      | Start of string                    |
| `$`      | End of string                      |
| `[...]`  | Any character in set               |
| `[^...]` | Any character **not** in set       |
| `*`      | 0 or more repetitions              |
| `+`      | 1 or more repetitions              |
| `{n}`    | Exactly n repetitions              |
| `{n,m}`  | Between n and m repetitions        |

---

## ✅ Example 1: Validate Email

```python
import re

email = "user@example.com"
pattern = r'^[\w\.-]+@[\w\.-]+\.\w+$'

if re.match(pattern, email):
    print("Valid email")
else:
    print("Invalid email")
```

---

## ✅ Example 2: Extract All Numbers

```python
text = "My phone number is 123-456-7890 and zip is 90210"
numbers = re.findall(r'\d+', text)
print(numbers)  # ['123', '456', '7890', '90210']
```

---

## ✅ Example 3: Replace Words

```python
text = "I love cats"
new_text = re.sub(r'cats', 'dogs', text)
print(new_text)  # I love dogs
```

---

## 🧠 Tip: Use Raw Strings (`r""`)

Always write patterns as **raw strings** to avoid escaping backslashes:

```python
pattern = r'\d+'  # NOT '\\d+'
```

---

## 🧰 Summary

| Tool           | Use Case                      |
| -------------- | ----------------------------- |
| `re.match()`   | Match from the beginning      |
| `re.search()`  | Search anywhere in the string |
| `re.findall()` | Find all matching substrings  |
| `re.sub()`     | Replace matched substrings    |

