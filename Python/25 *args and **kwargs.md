### ⭐ `*args` and `**kwargs` in Python

They allow you to **pass a variable number of arguments** to a function.

---

## 🔹 `*args` (Non-keyword arguments)

* Stands for "**arguments**"
* Collects extra **positional arguments** as a **tuple**

### ✅ Example:

```python
def add_numbers(*args):
    print(args)
    return sum(args)

print(add_numbers(1, 2, 3))   # (1, 2, 3) → 6
```

You can loop through `args`:

```python
def show_names(*args):
    for name in args:
        print("Hello", name)

show_names("Alice", "Bob", "Charlie")
```

---

## 🔹 `**kwargs` (Keyword arguments)

* Stands for "**keyword arguments**"
* Collects extra **named arguments** into a **dictionary**

### ✅ Example:

```python
def show_info(**kwargs):
    print(kwargs)

show_info(name="Alice", age=30)
# Output: {'name': 'Alice', 'age': 30}
```

You can loop through `kwargs`:

```python
def display_details(**kwargs):
    for key, value in kwargs.items():
        print(f"{key} = {value}")

display_details(name="Bob", course="Python", level="Beginner")
```

---

## 🔹 Using Both Together

```python
def demo(a, *args, **kwargs):
    print("a =", a)
    print("args =", args)
    print("kwargs =", kwargs)

demo(1, 2, 3, x=10, y=20)
```

**Output:**

```
a = 1
args = (2, 3)
kwargs = {'x': 10, 'y': 20}
```

---

## 🔁 When to Use

| Use this   | When                                                            |
| ---------- | --------------------------------------------------------------- |
| `*args`    | You don’t know how many **positional** arguments will be passed |
| `**kwargs` | You don’t know how many **keyword** arguments will be passed    |

