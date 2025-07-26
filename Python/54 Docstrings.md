### 📝 Python Docstrings

**Docstrings** are special strings used to document **what a function, class, or module does**. They are placed as the **first statement inside** the object (function, class, module).

They help:

* Others understand your code
* Generate documentation automatically
* Improve code readability

---

## 🔹 Basic Function Docstring

```python
def greet(name):
    """Return a greeting for the given name."""
    return f"Hello, {name}!"
```

You can access it with:

```python
print(greet.__doc__)  # Output: Return a greeting for the given name.
```

---

## 🔹 Multi-line Docstring Format (PEP 257)

```python
def divide(a, b):
    """
    Divide two numbers and return the result.

    Parameters:
    a (int or float): Numerator
    b (int or float): Denominator

    Returns:
    float: The result of division

    Raises:
    ZeroDivisionError: If b is zero
    """
    if b == 0:
        raise ZeroDivisionError("Cannot divide by zero.")
    return a / b
```

---

## 🔹 Class Docstring

```python
class Animal:
    """A class representing an animal."""

    def __init__(self, name):
        """Initialize the animal with a name."""
        self.name = name
```

---

## ✅ Best Practices

* Use triple double quotes (`"""doc"""`)
* Be concise but clear
* Mention:

  * Purpose
  * Parameters
  * Return value
  * Exceptions (if any)

---

## 🔹 Tools That Use Docstrings

* IDE tooltips (PyCharm, VS Code)
* Help system: `help(function)`
* Documentation generators (e.g. Sphinx, pdoc)

---

## 🧠 Summary

| Location     | Example Usage           |
| ------------ | ----------------------- |
| Function     | `def func(): """..."""` |
| Class        | `class C: """..."""`    |
| Module (top) | `"""This module..."""`  |

