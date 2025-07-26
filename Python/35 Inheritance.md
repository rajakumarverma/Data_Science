### 🧬 Inheritance in Python

**Inheritance** allows a class (called the **child** or **derived** class) to **inherit** attributes and methods from another class (called the **parent** or **base** class).
It promotes **code reuse**, **organization**, and **extensibility**.

---

## 🔹 Basic Syntax

```python
class Parent:
    # base class
    pass

class Child(Parent):
    # derived class
    pass
```

---

## ✅ Simple Example

```python
class Animal:
    def speak(self):
        print("This animal makes a sound.")

class Dog(Animal):
    def bark(self):
        print("The dog barks.")

# Usage
d = Dog()
d.speak()  # Inherited from Animal
d.bark()   # Defined in Dog
```

---

## 🔹 `super()` Function

Use `super()` to call the **parent class’s constructor** or methods.

```python
class Person:
    def __init__(self, name):
        self.name = name

class Student(Person):
    def __init__(self, name, grade):
        super().__init__(name)       # Call Person's __init__
        self.grade = grade
```

---

## 🔹 Types of Inheritance

| Type             | Description                                | Example                      |
| ---------------- | ------------------------------------------ | ---------------------------- |
| **Single**       | One child inherits from one parent         | `class B(A):`                |
| **Multilevel**   | A class inherits from a child class        | `class C(B):`                |
| **Multiple**     | A class inherits from **multiple** parents | `class C(A, B):`             |
| **Hierarchical** | Multiple classes inherit from one parent   | `class B(A):`, `class C(A):` |

---

## ✅ Example: Multilevel Inheritance

```python
class Vehicle:
    def start(self):
        print("Vehicle started")

class Car(Vehicle):
    def drive(self):
        print("Car is driving")

class ElectricCar(Car):
    def charge(self):
        print("Charging battery")

e = ElectricCar()
e.start()   # From Vehicle
e.drive()   # From Car
e.charge()  # From ElectricCar
```

---

## 🧠 Benefits of Inheritance

* Reuse code
* Easier to manage large codebases
* Supports polymorphism and method overriding
