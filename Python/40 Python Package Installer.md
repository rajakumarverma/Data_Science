### 📦 `pip` – Python Package Installer

`pip` is the **standard package manager for Python**.
It lets you **install**, **upgrade**, and **uninstall** third-party libraries and tools from [PyPI](https://pypi.org).

---

## 🔹 Basic Commands

| Command                              | Description                  |
| ------------------------------------ | ---------------------------- |
| `pip install package_name`           | Install a package            |
| `pip uninstall package_name`         | Remove a package             |
| `pip install --upgrade package_name` | Upgrade a package            |
| `pip list`                           | Show installed packages      |
| `pip show package_name`              | Show details about a package |

---

## ✅ Example: Install `requests`

```bash
pip install requests
```

Use it in Python:

```python
import requests

response = requests.get("https://api.github.com")
print(response.status_code)
```

---

## 🔹 Installing Specific Versions

```bash
pip install numpy==1.24.0
```

---

## 🔹 Install from a `requirements.txt` file

This file lists all dependencies:

**`requirements.txt`**

```
requests
pandas>=1.4.0
flask==2.3.2
```

Then install everything at once:

```bash
pip install -r requirements.txt
```

---

## 🔹 Uninstall a Package

```bash
pip uninstall requests
```

---

## 🔹 Check if pip is installed

```bash
pip --version
```

If not, install it using:

```bash
python -m ensurepip --upgrade
```

---

## 🧠 Tip: Use a Virtual Environment

To avoid messing with global Python packages, use:

```bash
python -m venv env
source env/bin/activate   # On Mac/Linux
env\Scripts\activate      # On Windows
```

Then install packages locally.

