### 🎀 Decorators in Python

A **decorator** is a **function that modifies another function**, adding extra behavior **before or after** the original function runs — without changing its code.

It's often used for:

* Logging
* Authentication
* Timing
* Access control
* Caching

---

## 🔹 Basic Syntax

```python
def decorator_function(original_function):
    def wrapper():
        print("Before the function runs")
        original_function()
        print("After the function runs")
    return wrapper
```

Then apply it:

```python
@decorator_function
def say_hello():
    print("Hello!")

say_hello()
```

---

## ✅ Output:

```
Before the function runs
Hello!
After the function runs
```

---

## 🔹 Example with `*args` and `**kwargs`

```python
def debug(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with {args} {kwargs}")
        return func(*args, **kwargs)
    return wrapper

@debug
def add(a, b):
    return a + b

print(add(3, 4))  # Output: Calling add with (3, 4) {}
                 #         7
```

---

## ✅ Multiple Decorators

```python
def bold(func):
    def wrapper():
        return "<b>" + func() + "</b>"
    return wrapper

def italic(func):
    def wrapper():
        return "<i>" + func() + "</i>"
    return wrapper

@bold
@italic
def greet():
    return "Hello"

print(greet())  # <b><i>Hello</i></b>
```

---

## ✅ Built-in Decorators Example

* `@staticmethod`
* `@classmethod`
* `@property`

---

## 🧠 Summary

| Feature           | Description                                |
| ----------------- | ------------------------------------------ |
| `@decorator`      | Short-hand to wrap a function              |
| `*args, **kwargs` | Allow decorators to work with any function |
| Reusable          | Keeps code DRY and modular                 |

