### 🧩 Class Methods in Python

A **class method** is a method that belongs to the **class itself**, not just to instances (objects).
It can **access and modify class-level data**, and is defined using the `@classmethod` decorator.

---

## 🔹 Syntax

```python
class MyClass:
    @classmethod
    def my_class_method(cls, args):
        # cls refers to the class, not the instance
```

---

## ✅ Example

```python
class Dog:
    species = "Canine"  # Class variable

    def __init__(self, name):
        self.name = name

    @classmethod
    def get_species(cls):
        return f"All dogs are {cls.species}"

# Usage
print(Dog.get_species())  # All dogs are Canine
```

* `cls` is like `self`, but refers to the **class**, not the **instance**.
* You can call class methods on both the class and its objects.

---

## 🔹 Modify Class Variable Using Class Method

```python
class Counter:
    count = 0

    @classmethod
    def increment(cls):
        cls.count += 1

Counter.increment()
Counter.increment()
print(Counter.count)  # 2
```

---

## 🔹 Difference: `@classmethod` vs `@staticmethod` vs instance methods

| Type            | Access to `self` | Access to `cls` | Access class/instance data |
| --------------- | ---------------- | --------------- | -------------------------- |
| Instance Method | ✅ Yes            | ❌ No            | ✅ Yes                      |
| Class Method    | ❌ No             | ✅ Yes           | ✅ Class only               |
| Static Method   | ❌ No             | ❌ No            | ❌ (Utility method)         |

---

## 🔹 Use Cases for `@classmethod`

* Creating factory methods (alternative constructors)
* Accessing or modifying **class-level data**
* Defining behaviors shared across all instances

---

### ✅ Factory Method Example

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    @classmethod
    def from_birth_year(cls, name, birth_year):
        from datetime import datetime
        current_year = datetime.now().year
        age = current_year - birth_year
        return cls(name, age)

p = Person.from_birth_year("Alice", 2000)
print(p.name, p.age)
```
