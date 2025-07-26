### 🧩 `if __name__ == "__main__"` in Python

This line is used to **control the execution** of your code — especially when your script can be **both run directly or imported as a module**.

---

## 🔹 What It Means

```python
if __name__ == "__main__":
    # Run this code only when the script is executed directly
```

---

## ✅ Why Use It?

* Prevents certain code from running when the file is **imported**
* Useful for writing reusable **modules**
* Great for running **tests or main logic** in a controlled way

---

## 🔍 How It Works

Python sets a special built-in variable:

| Condition                  | `__name__` value |
| -------------------------- | ---------------- |
| Script is **run directly** | `"__main__"`     |
| Script is **imported**     | `module_name`    |

---

## 🔧 Example

### File: `greet.py`

```python
def say_hello():
    print("Hello!")

if __name__ == "__main__":
    say_hello()
```

### File: `main.py`

```python
import greet  # Imports without running say_hello()
```

Output:

```
(Only runs when greet.py is executed directly, not when imported.)
```

---

## ✅ Use Case: Entry Point for a Program

```python
def main():
    print("Program is running...")

if __name__ == "__main__":
    main()
```

---

## 🧠 Summary

| Purpose                       | Explanation                                           |
| ----------------------------- | ----------------------------------------------------- |
| Entry point check             | Ensures certain code runs only when executed directly |
| Reusability                   | Keeps modules clean and import-safe                   |
| Common in CLI tools & scripts | Helps define where a program "starts"                 |

