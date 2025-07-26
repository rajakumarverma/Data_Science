### 🔤 String Indexing in Python

**String indexing** allows you to access individual characters in a string using their **position (index)**.

---

## 🔹 How Indexing Works

In Python, strings are ordered sequences of characters.
Each character has a position (index), starting from **0**.

```python
text = "Python"
# Index:    0 1 2 3 4 5
# Reverse: -6-5-4-3-2-1
```

---

## ✅ Accessing Characters

```python
text = "Python"
print(text[0])   # P
print(text[3])   # h
print(text[-1])  # n (last character)
```

---

## 🛑 Index Out of Range

Accessing an index that doesn't exist will raise an error:

```python
print(text[10])  # IndexError
```

---

## 🔄 Looping Through a String (Optional)

```python
for char in "Hi":
    print(char)
```

---

## 🔍 Use Case: First and Last Letters

```python
word = "apple"
print("First:", word[0])
print("Last:", word[-1])
```

---

## 🔐 Strings Are Immutable

You **cannot** change a character by index directly:

```python
text = "Hello"
# text[0] = "Y"  ❌ This gives TypeError
```

But you can create a new string:

```python
text = "Hello"
new_text = "Y" + text[1:]  # "Yello"
print(new_text)
```
