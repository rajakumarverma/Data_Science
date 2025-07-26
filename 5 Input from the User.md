### ⌨️ Getting Input from the User in Python

Python uses the **`input()`** function to take input from the user via the keyboard.

---

## 🔹 Basic Syntax

```python
variable = input("Prompt message: ")
```

> This always returns a **string**!

---

### ✅ Example:

```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
```

**Output:**

```
Enter your name: Alice
Hello, Alice!
```

---

## 🔁 Convert Input to Other Types (Type Casting)

Since `input()` returns a **string**, you must convert it if you want a number or boolean.

### 🔹 Example: Get Integer Input

```python
age = int(input("Enter your age: "))
print("You will be", age + 1, "next year.")
```

### 🔹 Example: Get Float Input

```python
price = float(input("Enter price: "))
print("Total with tax:", price * 1.15)
```

### 🔹 Example: Boolean Input

```python
response = input("Do you agree? (yes/no): ")
is_agree = response.lower() == "yes"
print("Agreed:", is_agree)
```

---

## 🛑 Tip: Always Validate User Input (Optional)

User might enter something invalid. You can use `try`/`except`:

```python
try:
    number = int(input("Enter a number: "))
    print("Double:", number * 2)
except ValueError:
    print("That's not a valid number!")
```
