### 🛠️ Feature Engineering in Python — Handling Missing Values

**Feature engineering** is the process of transforming raw data into features that better represent the underlying problem to the predictive models. A key step is handling **missing values**.

---

## 🔍 Step 1: Detect Missing Values

```python
import pandas as pd

df = pd.read_csv('your_data.csv')
print(df.isnull().sum())  # Count of missing values per column
```

---

## 🔄 Step 2: Handling Missing Values

### 1. **Drop Missing Values**

#### 🔹 Drop rows:

```python
df_cleaned = df.dropna()
```

#### 🔹 Drop columns:

```python
df_cleaned = df.dropna(axis=1)
```

---

### 2. **Fill Missing Values (Imputation)**

#### 🔹 Fill with a constant:

```python
df['column'] = df['column'].fillna(0)
df['city'] = df['city'].fillna('Unknown')
```

#### 🔹 Fill with statistical values:

```python
df['age'] = df['age'].fillna(df['age'].mean())      # Mean
df['income'] = df['income'].fillna(df['income'].median())  # Median
df['category'] = df['category'].fillna(df['category'].mode()[0])  # Mode
```

---

### 3. **Forward / Backward Fill**

```python
df['value'].fillna(method='ffill', inplace=True)  # forward fill
df['value'].fillna(method='bfill', inplace=True)  # backward fill
```

---

### 4. **Use Interpolation**

For numerical, ordered data (e.g. time series):

```python
df['value'] = df['value'].interpolate()
```

---

### 5. **Use Scikit-learn Imputer (Advanced)**

```python
from sklearn.impute import SimpleImputer

imputer = SimpleImputer(strategy='mean')
df[['age']] = imputer.fit_transform(df[['age']])
```

Other strategies: `'mean'`, `'median'`, `'most_frequent'`, `'constant'`

---

## 📌 Pro Tip: Visualize Missing Data

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.heatmap(df.isnull(), cbar=False, cmap='viridis')
plt.show()
```

---

## 🧠 Best Practices

| Situation            | Recommended Action                 |
| -------------------- | ---------------------------------- |
| <5% values missing   | Drop rows                          |
| >5% but not critical | Fill with mean/median/mode         |
| Time series          | Use `.interpolate()` or `.ffill()` |
| Categorical columns  | Fill with `'Unknown'` or `mode()`  |
| Advanced models      | Use sklearn imputers or KNN        |

