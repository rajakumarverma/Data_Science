### 🖨️ Output in Python – `print()` Function

The `print()` function is used to **display output to the screen**.

---

## 🔹 Basic Syntax

```python
print(value1, value2, ..., sep=' ', end='\n')
```

* `value1, value2, ...`: Items to print
* `sep`: Separator between values (default is space `' '`)
* `end`: What to print at the end (default is newline `'\n'`)

---

## ✅ Examples

### 🔸 Print a single value

```python
print("Hello, World!")
```

### 🔸 Print multiple values

```python
name = "Alice"
age = 25
print(name, age)
# Output: Alice 25
```

---

## 🔹 Formatting Output

### 1. **f-strings** (Recommended in Python 3.6+)

```python
name = "Bob"
score = 90
print(f"{name} scored {score} points.")
```

### 2. **`str.format()` method**

```python
print("{} scored {} points.".format(name, score))
```

---

## 🔹 Custom Separators and Endings

### 🔸 `sep` (separator between values)

```python
print("Python", "Java", "C++", sep=", ")
# Output: Python, Java, C++
```

### 🔸 `end` (what to print at the end)

```python
print("Loading", end="...")
print("Done!")
# Output: Loading...Done!
```

---

## 🔹 Printing Without a Newline

```python
print("Hello", end=" ")
print("World")
# Output: Hello World
```

---

## 🧠 Fun Example

```python
name = input("Enter your name: ")
print(f"Welcome, {name}! 🎉")
```
