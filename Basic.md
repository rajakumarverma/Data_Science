# 🐍 Python Basics Cheat Sheet

> Outputs are shown right inside the code blocks as comments for clarity.

---

## 1. Variable Assignment

```python
x = 10
name = "Alice"
# (No output, stores values)
```

---

## 2. Variable Naming Rules

- Start with letter or `_`
- Use letters, numbers, and `_`
- Case-sensitive, no keywords

---

## 3. Data Types

`int`, `float`, `str`, `bool`, `list`, `tuple`, `dict`, `set`, `None`

---

## 4. Type Checking

```python
type(x)           # <class 'int'>
isinstance(x, int) # True
```

---

## 5. Type Casting

```python
int("5")         # 5
float("3.14")    # 3.14
str(10)          # '10'
```

---

## 6. Input from User

```python
name = input("Enter name: ")  # User types: Bob
print(name)                   # Bob
```

---

## 7. Output Print

```python
print("Hello", name)   # Hello Bob
print(f"Hi, {name}")   # Hi, Bob
```

---

## 8. String Indexing

```python
s = "Python"
print(s[0], s[-1])     # P n
```

---

## 9. String Slicing

```python
print(s[1:4])          # yth
print(s[:3])           # Pyt
print(s[3:])           # hon
```

---

## 10. String Methods

```python
"hello".upper()         # HELLO
"HELLO".lower()         # hello
"abc".replace("a", "z") # zbc
```

---

## 11. Arithmetic Operators

```python
7 + 3     # 10
7 / 3     # 2.3333
7 // 3    # 2
7 % 3     # 1
2 ** 3    # 8
```

---

## 12. Comparison Operators

```python
5 == 5    # True
5 != 3    # True
3 > 2     # True
3 <= 3    # True
```

---

## 13. Logical Operators

```python
True and False   # False
True or False    # True
not True         # False
```

---

## 14. Membership Operators

```python
'a' in "apple"       # True
3 not in [1, 2, 4]   # True
```

---

## 15. Identity Operators

```python
a = [1, 2]
b = a
a is b              # True
a is not [1, 2]     # True
```

---

## 16. if / elif / else

```python
x = 5
if x > 0:
    print("Positive")     # Positive
elif x == 0:
    print("Zero")
else:
    print("Negative")
```

---

## 17. for Loop

```python
for i in range(3):
    print(i)
# Output:
# 0
# 1
# 2
```

---

## 18. while Loop

```python
i = 0
while i < 3:
    print(i)
    i += 1
# Output:
# 0
# 1
# 2
```

---

## 19. break / continue

```python
for i in range(5):
    if i == 3:
        break
    if i == 1:
        continue
    print(i)
# Output:
# 0
# 2
```

---

## 20. range() Function

```python
list(range(5))        # [0, 1, 2, 3, 4]
list(range(1, 5))     # [1, 2, 3, 4]
list(range(0, 10, 2)) # [0, 2, 4, 6, 8]
```

---

## 21. List

```python
fruits = ["apple", "banana"]
print(fruits)          # ['apple', 'banana']
```

---

## 22. List Indexing

```python
fruits[0]              # 'apple'
fruits[-1]             # 'banana'
```

---

## 23. List Slicing

```python
fruits[0:1]            # ['apple']
fruits[1:]             # ['banana']
```

---

## 24. List Methods

```python
fruits.append("orange")
print(fruits)          # ['apple', 'banana', 'orange']

fruits.remove("banana")
print(fruits)          # ['apple', 'orange']
```

---

## 25. Tuple

```python
colors = ("red", "green")
print(colors[0])       # 'red'
```

---

## 26. Set

```python
nums = {1, 2, 2, 3}
print(nums)            # {1, 2, 3}
```

---

## 27. Dictionary

```python
person = {"name": "Alice", "age": 30}
print(person["name"])  # Alice
```

---

## 28. Function

```python
def greet(name):
    print(f"Hello, {name}")

greet("Bob")           # Hello, Bob
```

---

## 29. *args and **kwargs

```python
def example(*args, **kwargs):
    print(args)
    print(kwargs)

example(1, 2, name="Alice")
# Output:
# (1, 2)
# {'name': 'Alice'}
```

---

## 30. return Statement

```python
def square(x):
    return x * x

print(square(4))       # 16
```

---
