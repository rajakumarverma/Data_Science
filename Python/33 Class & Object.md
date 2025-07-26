### 🧱 Class & Object in Python

Python is an **object-oriented programming** (OOP) language.
Classes and objects are the core building blocks of OOP.

---

## 🔹 What is a **Class**?

A **class** is a **blueprint** for creating objects.
It defines **attributes** (variables) and **methods** (functions) that the objects will have.

### ✅ Example:

```python
class Person:
    def __init__(self, name, age):  # Constructor
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello, my name is {self.name}.")
```

---

## 🔹 What is an **Object**?

An **object** is an **instance** of a class.

### ✅ Creating an Object:

```python
p1 = Person("Alice", 25)  # Object of Person class
p1.greet()  # Output: Hello, my name is Alice.
```

---

## 🔹 `__init__()` Method (Constructor)

* A **special method** that runs automatically when an object is created.
* It’s used to **initialize attributes**.

```python
def __init__(self, name):
    self.name = name
```

---

## 🔹 `self` Keyword

* Refers to the **current object**.
* Used to access attributes and methods from within the class.

---

## 🔹 Accessing Attributes & Methods

```python
print(p1.name)     # Alice
print(p1.age)      # 25
p1.greet()         # Hello, my name is Alice.
```

---

## 🧠 Summary

| Term       | Description                       |
| ---------- | --------------------------------- |
| `class`    | Blueprint for creating objects    |
| `object`   | Instance of a class               |
| `__init__` | Constructor for initializing data |
| `self`     | Refers to the current instance    |

---

### Bonus: Example with Multiple Methods

```python
class Calculator:
    def __init__(self, a, b):
        self.a = a
        self.b = b

    def add(self):
        return self.a + self.b

    def multiply(self):
        return self.a * self.b

c = Calculator(3, 5)
print(c.add())        # 8
print(c.multiply())   # 15
```
