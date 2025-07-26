### 🔢 Label Encoding vs Ordinal Encoding in Python

When handling **categorical data**, you often need to convert it into **numerical form** for machine learning models. Two common encoding techniques are:

---

## 🟦 1. **Label Encoding**

* Converts each **category into a unique integer**.
* No implied order — useful for **non-ordinal** categories.
* Can cause problems if model assumes numeric order.

### ✅ Example:

```python
from sklearn.preprocessing import LabelEncoder
import pandas as pd

df = pd.DataFrame({'City': ['London', 'Paris', 'New York', 'Paris', 'London']})

le = LabelEncoder()
df['City_encoded'] = le.fit_transform(df['City'])

print(df)
```

**Output:**

```
       City  City_encoded
0    London             1
1     Paris             2
2  New York             0
3     Paris             2
4    London             1
```

> ⚠️ Models might think Paris > London > New York, which may not make sense!

---

## 🟧 2. **Ordinal Encoding**

* Use when your categorical variable has a **meaningful order** (ordinal scale).
* Example: `Low < Medium < High`, or `Beginner < Intermediate < Expert`

### ✅ Manual Ordinal Mapping:

```python
df = pd.DataFrame({'Size': ['Small', 'Medium', 'Large', 'Medium']})

size_map = {'Small': 0, 'Medium': 1, 'Large': 2}
df['Size_encoded'] = df['Size'].map(size_map)

print(df)
```

---

### ✅ Using `OrdinalEncoder` from Scikit-learn:

```python
from sklearn.preprocessing import OrdinalEncoder

df = pd.DataFrame({'Size': ['Small', 'Medium', 'Large', 'Medium']})
encoder = OrdinalEncoder(categories=[['Small', 'Medium', 'Large']])
df['Size_encoded'] = encoder.fit_transform(df[['Size']])

print(df)
```

---

## 🧠 Summary Table

| Encoding Type    | Use Case               | Caution                              |
| ---------------- | ---------------------- | ------------------------------------ |
| Label Encoding   | Non-ordinal categories | Model may assume numerical order     |
| Ordinal Encoding | Ordered categories     | Must preserve correct order manually |

---

### 🧪 Tip:

For **non-ordinal categorical features**, it's usually safer to use **One-Hot Encoding** instead of Label Encoding to avoid misleading models.
