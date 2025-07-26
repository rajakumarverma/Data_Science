### 🧪 Python Virtual Environment (`venv`)

A **virtual environment** is a self-contained directory that contains a Python installation for a particular project. It helps **isolate dependencies** so they don’t conflict between projects.

---

## ✅ Why Use a Virtual Environment?

* Keeps project dependencies separate
* Avoids version conflicts
* Makes deployments and collaboration cleaner

---

## 🔹 Create a Virtual Environment

```bash
python -m venv venv_name
```

Example:

```bash
python -m venv myenv
```

This creates a folder called `myenv/` containing a local Python environment.

---

## 🔹 Activate the Virtual Environment

| OS          | Command                     |
| ----------- | --------------------------- |
| Windows     | `myenv\Scripts\activate`    |
| macOS/Linux | `source myenv/bin/activate` |

You’ll see something like this in your terminal:

```
(myenv) $
```

---

## 🔹 Install Packages Inside It

```bash
pip install package-name
```

Example:

```bash
pip install requests
```

Packages will be installed **only inside** `myenv`.

---

## 🔹 Freeze Installed Packages

```bash
pip freeze > requirements.txt
```

This creates a list of dependencies (great for sharing with others).

---

## 🔹 Reinstall from `requirements.txt`

```bash
pip install -r requirements.txt
```

---

## 🔹 Deactivate the Environment

```bash
deactivate
```

Returns to the system’s default Python environment.

---

## 🧠 Summary

| Task                      | Command                           |
| ------------------------- | --------------------------------- |
| Create environment        | `python -m venv myenv`            |
| Activate (Windows)        | `myenv\Scripts\activate`          |
| Activate (macOS/Linux)    | `source myenv/bin/activate`       |
| Deactivate                | `deactivate`                      |
| Install packages          | `pip install <pkg>`               |
| Export packages           | `pip freeze > requirements.txt`   |
| Install from requirements | `pip install -r requirements.txt` |

