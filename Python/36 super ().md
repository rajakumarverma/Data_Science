### 🔗 `super()` in Python

The `super()` function is used to **call a method from the parent class**, most commonly the `__init__()` constructor.
It’s a key tool when working with **inheritance**.

---

## 🔹 Why use `super()`?

* Avoids manually referencing the parent class
* Makes your code **cleaner**, especially in **multiple inheritance**
* Ensures proper **method resolution order (MRO)**

---

## ✅ Basic Example

```python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)  # calls Animal's __init__
        self.breed = breed

d = Dog("Buddy", "Labrador")
print(d.name)   # Buddy
print(d.breed)  # Labrador
```

---

## 🔹 Without `super()`

```python
class Dog(Animal):
    def __init__(self, name, breed):
        Animal.__init__(self, name)  # works, but less flexible
        self.breed = breed
```

✅ Works, but hard-coding the parent class (`Animal`) is discouraged.

---

## 🔹 `super()` in Method Overriding

```python
class A:
    def greet(self):
        print("Hello from A")

class B(A):
    def greet(self):
        super().greet()
        print("Hello from B")

b = B()
b.greet()
```

**Output:**

```
Hello from A  
Hello from B
```

---

## 🔹 In Multiple Inheritance

```python
class A:
    def show(self):
        print("A")

class B(A):
    def show(self):
        super().show()
        print("B")

class C(B):
    def show(self):
        super().show()
        print("C")

c = C()
c.show()
```

**Output (MRO-based):**

```
A  
B  
C
```

---

## 🧠 Summary

| Feature   | Description                                  |
| --------- | -------------------------------------------- |
| `super()` | Calls a method from the parent class         |
| Use case  | Mostly in constructors or overridden methods |
| Benefit   | Avoids hardcoding, follows MRO               |

