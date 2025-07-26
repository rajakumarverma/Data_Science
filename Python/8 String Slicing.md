### ✂️ String Slicing in Python

**String slicing** allows you to extract a part (substring) of a string using **start**, **end**, and **step** values.

---

## 🔹 Syntax

```python
string[start:end:step]
```

* `start`: index to begin (inclusive)
* `end`: index to stop (exclusive)
* `step`: how many steps to move (optional)

---

## ✅ Examples

```python
text = "Python"

print(text[0:2])     # 'Py'      (index 0 and 1)
print(text[1:4])     # 'yth'     (index 1 to 3)
print(text[:3])      # 'Pyt'     (from start to index 2)
print(text[3:])      # 'hon'     (from index 3 to end)
print(text[:])       # 'Python'  (full copy)
```

---

## 🔄 Step Slicing

```python
print(text[::2])     # 'Pto'  (every 2nd character)
print(text[::-1])    # 'nohtyP' (reversed string)
```

---

## 🔍 Negative Indexes Work Too

```python
print(text[-4:-1])   # 'tho'
```

---

## 📦 Real Example

```python
word = "Programming"
print(word[3:8])     # 'gramm'
print(word[-5:])     # 'mming'
print(word[::-1])    # 'gnimmargorP'
```

---

## ❗ Remember

* `text[a:b]` gives characters from index `a` to `b-1`
* It doesn't raise an error if indexes go out of range:

  ```python
  print(text[0:100])  # returns up to end if 100 is too big
  ```
