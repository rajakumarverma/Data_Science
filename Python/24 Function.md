### 🧩 Function in Python

A **function** is a reusable block of code that performs a specific task.
Functions help make code **modular**, **readable**, and **easy to maintain**.

---

## 🔹 Defining a Function

```python
def function_name():
    # code block
```

### ✅ Example:

```python
def greet():
    print("Hello, world!")

greet()  # Call the function
```

---

## 🔹 Function with Parameters

```python
def greet(name):
    print("Hello,", name)

greet("Alice")  # Output: Hello, Alice
```

---

## 🔹 Function with Return Value

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # 8
```

---

## 🔹 Default Parameters

```python
def greet(name="Guest"):
    print("Hello,", name)

greet()         # Hello, Guest
greet("Bob")    # Hello, Bob
```

---

## 🔹 Keyword Arguments

```python
def profile(name, age):
    print(f"Name: {name}, Age: {age}")

profile(age=25, name="Alice")
```

---

## 🔹 Arbitrary Arguments

### `*args` – Multiple Positional Arguments

```python
def total(*numbers):
    return sum(numbers)

print(total(1, 2, 3))  # 6
```

### `**kwargs` – Multiple Keyword Arguments

```python
def display_info(**info):
    for key, value in info.items():
        print(f"{key}: {value}")

display_info(name="John", age=30)
```

---

## 🧠 Function Scope

* **Local Variable**: Defined inside a function
* **Global Variable**: Defined outside all functions

```python
x = 10  # Global

def show():
    x = 5  # Local
    print(x)

show()     # 5
print(x)   # 10
```

---

## 🧪 Lambda Function (Anonymous Function)

```python
square = lambda x: x * x
print(square(4))  # 16
```
