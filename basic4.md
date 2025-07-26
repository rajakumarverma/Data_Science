### 45. Generator Function

Generate items one by one, saving memory.

```python
def count_up_to(n):
    count = 1
    while count <= n:
        yield count
        count += 1

for num in count_up_to(3):
    print(num)
# 1
# 2
# 3
```

---

### 53. Iterators

Objects you can loop over.

```python
nums = [1, 2, 3]
it = iter(nums)
print(next(it))  # 1
print(next(it))  # 2
```

---

### 54. Decorators

Modify functions without changing them.

```python
def decorator(func):
    def wrapper():
        print("Before")
        func()
        print("After")
    return wrapper

@decorator
def say_hello():
    print("Hello")

say_hello()
# Before
# Hello
# After
```

---

### 55. Regular Expressions

Pattern matching in strings (import `re`).

```python
import re
pattern = r'\d+'
result = re.findall(pattern, 'There are 12 apples and 34 oranges')
print(result)  # ['12', '34']
```

---

### 56. JSON Parsing

Work with JSON data.

```python
import json
data = '{"name": "Alice", "age": 30}'
parsed = json.loads(data)
print(parsed['name'])  # Alice
```

---

### 57. Date & Time

Work with dates and times.

```python
from datetime import datetime
now = datetime.now()
print(now.strftime("%Y-%m-%d %H:%M:%S"))
```

---

### 58. Math / Random Lib

Useful math functions and random numbers.

```python
import math, random
print(math.pi)          # 3.141592653589793
print(random.randint(1, 10))  # random number 1-10
```

---

### 59. SQLite DB Access

Basic database interaction.

```python
import sqlite3
conn = sqlite3.connect(':memory:')
c = conn.cursor()
c.execute('CREATE TABLE test(id INTEGER)')
conn.close()
```

---

### 60. Virtual Env

Isolate project dependencies (run in terminal).

```bash
python -m venv env
source env/bin/activate  # Linux/Mac
env\Scripts\activate     # Windows
```

---

### 61. Web Scraping

Extract data from websites.

```python
import requests
from bs4 import BeautifulSoup

r = requests.get('https://example.com')
soup = BeautifulSoup(r.text, 'html.parser')
print(soup.title.text)
```

---

### 62. Pandas (Basic)

Powerful data analysis tool.

```python
import pandas as pd
df = pd.DataFrame({'A':[1,2], 'B':[3,4]})
print(df)
```

---

### 63. NumPy (Basic)

Efficient numerical computing.

```python
import numpy as np
arr = np.array([1, 2, 3])
print(arr * 2)  # [2 4 6]
```

---

### 64. Docstrings

Documentation inside functions/classes.

```python
def greet():
    """Prints a greeting message."""
    print("Hello")

print(greet.__doc__)  # Prints docstring
```

---

### 65. `__name__ == "__main__"`

Run code only if script is executed directly.

```python
def main():
    print("Run directly")

if __name__ == "__main__":
    main()
```
