### 🔀 `if / elif / else` in Python

The `if`, `elif`, and `else` statements are used to **control the flow** of your program based on conditions.

---

## 🔹 Syntax

```python
if condition1:
    # code block 1
elif condition2:
    # code block 2
else:
    # code block 3
```

* **`if`** checks the first condition
* **`elif`** (short for *else if*) checks additional conditions if `if` is false
* **`else`** runs if none of the above conditions are true

---

## ✅ Basic Example

```python
x = int(input("Enter a number: "))

if x > 0:
    print("Positive number")
elif x < 0:
    print("Negative number")
else:
    print("Zero")
```

---

## 🔹 Multiple `elif`s Allowed

```python
marks = int(input("Enter your score: "))

if marks >= 90:
    print("Grade: A")
elif marks >= 80:
    print("Grade: B")
elif marks >= 70:
    print("Grade: C")
else:
    print("Grade: F")
```

---

## 🔍 Single-Line `if`

```python
age = 20
if age >= 18: print("Adult")
```

---

## 🧠 Boolean Conditions

You can use `and`, `or`, and `not`:

```python
temp = 25

if temp > 20 and temp < 30:
    print("Nice weather")
```

---

## 🚫 Indentation is Mandatory

Each block must be **indented** (usually 4 spaces):

```python
if True:
    print("This is indented correctly")
# Incorrect indentation will cause an error
```
