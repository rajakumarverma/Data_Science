### 🧰 String Methods in Python

Python provides **built-in methods** to work with strings easily. These methods do **not change the original string** (strings are immutable); they return **new strings**.

---

## 🔹 Commonly Used String Methods

| Method              | Description                             | Example                                  |
| ------------------- | --------------------------------------- | ---------------------------------------- |
| `lower()`           | Converts to lowercase                   | `"PYTHON".lower()` → `'python'`          |
| `upper()`           | Converts to uppercase                   | `"python".upper()` → `'PYTHON'`          |
| `title()`           | Capitalizes first letter of each word   | `"hello world".title()`                  |
| `strip()`           | Removes leading/trailing whitespace     | `"  hello  ".strip()` → `'hello'`        |
| `replace(old, new)` | Replaces substring                      | `"car".replace("c", "b")` → `'bar'`      |
| `find(sub)`         | Returns index of first occurrence       | `"hello".find("l")` → `2`                |
| `count(sub)`        | Counts occurrences                      | `"hello".count("l")` → `2`               |
| `startswith(sub)`   | Checks if starts with substring         | `"hello".startswith("he")`               |
| `endswith(sub)`     | Checks if ends with substring           | `"hello".endswith("lo")`                 |
| `split(delimiter)`  | Splits into a list                      | `"a,b,c".split(",")` → `['a', 'b', 'c']` |
| `join(iterable)`    | Joins elements with string as separator | `"-".join(['a','b'])` → `'a-b'`          |

---

## ✅ Examples

```python
text = "  Python Programming  "

print(text.lower())        # '  python programming  '
print(text.strip())        # 'Python Programming'
print(text.title())        # 'Python Programming'
print(text.replace("Python", "Java"))  # '  Java Programming  '
print(text.find("Prog"))   # 9
```

---

## 🔄 Example: Splitting and Joining

```python
sentence = "apple,banana,grape"
fruits = sentence.split(",")     # ['apple', 'banana', 'grape']
print(fruits)

joined = "-".join(fruits)        # 'apple-banana-grape'
print(joined)
```

---

## ✅ Boolean String Methods (Return True/False)

```python
text = "Hello123"

print(text.isalpha())    # False (contains digits)
print(text.isdigit())    # False
print("123".isdigit())   # True
print("abc".isalpha())   # True
```
