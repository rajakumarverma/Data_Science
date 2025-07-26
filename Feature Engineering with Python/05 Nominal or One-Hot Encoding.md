### 🔡 Data Encoding in Python — Nominal / One-Hot Encoding

When working with **categorical data**, most ML algorithms require **numerical input**. So we convert categories using **encoding techniques**.

---

## 📌 Nominal vs Ordinal

| Type        | Example                      | Encoding Type               |
| ----------- | ---------------------------- | --------------------------- |
| **Nominal** | Color: Red, Blue, Green      | One-Hot Encoding            |
| **Ordinal** | Size: Small < Medium < Large | Label Encoding (with order) |

---

## 🛠️ One-Hot Encoding (Nominal)

### 🔹 Using `pandas.get_dummies()`

```python
import pandas as pd

df = pd.DataFrame({
    'Color': ['Red', 'Green', 'Blue', 'Red']
})

df_encoded = pd.get_dummies(df, columns=['Color'])
print(df_encoded)
```

**Output:**

```
   Color_Blue  Color_Green  Color_Red
0           0            0          1
1           0            1          0
2           1            0          0
3           0            0          1
```

---

### 🔹 Using `sklearn.preprocessing.OneHotEncoder`

```python
from sklearn.preprocessing import OneHotEncoder

encoder = OneHotEncoder(sparse=False)
encoded = encoder.fit_transform(df[['Color']])

print(encoded)
print(encoder.get_feature_names_out(['Color']))
```

---

### 🔹 Drop First Column to Avoid Dummy Variable Trap

```python
pd.get_dummies(df, columns=['Color'], drop_first=True)
```

---

## 🟨 Label Encoding (For Ordinal Data)

```python
from sklearn.preprocessing import LabelEncoder

df = pd.DataFrame({'Size': ['Small', 'Medium', 'Large']})
encoder = LabelEncoder()
df['Size_encoded'] = encoder.fit_transform(df['Size'])

# If ordinal, better use mapping
df['Size_encoded'] = df['Size'].map({'Small': 0, 'Medium': 1, 'Large': 2})
```

---

## 🧠 When to Use What?

| Encoding Type      | Use Case                           |
| ------------------ | ---------------------------------- |
| `pd.get_dummies()` | Small datasets with few categories |
| `OneHotEncoder`    | Pipelines / Larger workflows       |
| `LabelEncoder`     | Ordinal categories                 |
| `map()`            | Custom ordinal order               |

---

## 📊 Example with Multiple Features

```python
df = pd.DataFrame({
    'Gender': ['Male', 'Female', 'Female'],
    'Color': ['Red', 'Green', 'Blue']
})

df_encoded = pd.get_dummies(df, drop_first=True)
print(df_encoded)
```

