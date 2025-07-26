### 🔄 `while` Loop in Python

A `while` loop is used to **repeat a block of code** **as long as a condition is `True`**.

---

## 🔹 Syntax

```python
while condition:
    # code block
```

* The loop runs **until** the condition becomes **False**.
* You **must** update something inside the loop to avoid an **infinite loop**.

---

## ✅ Basic Example

```python
i = 0
while i < 5:
    print(i)
    i += 1
```

**Output:**

```
0
1
2
3
4
```

---

## 🔹 Infinite Loop (⚠️ Use with caution!)

```python
while True:
    print("This will run forever unless you break it!")
    break  # stops the loop
```

---

## 🔹 `while` with `else`

```python
x = 3
while x > 0:
    print(x)
    x -= 1
else:
    print("Loop ended")
```

---

## 🔹 Using `break` and `continue`

```python
x = 0
while x < 5:
    x += 1
    if x == 3:
        continue  # skips this iteration
    if x == 5:
        break     # exits loop early
    print(x)
```

---

## 🧠 Example: User Input Until Correct

```python
password = ""
while password != "admin123":
    password = input("Enter password: ")

print("Access granted!")
```
