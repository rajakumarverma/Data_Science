### 🚨 Handling Outliers in Python

**Outliers** are data points that are significantly different from others — they can **skew your analysis and degrade model performance**.

---

## 🔍 Step 1: Detect Outliers

### 📊 1.1 Visual Methods

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.boxplot(data=df['column'])   # Boxplot
plt.show()

sns.histplot(df['column'], kde=True)  # Histogram
plt.show()
```

### 📏 1.2 Statistical Methods

#### IQR (Interquartile Range)

```python
Q1 = df['column'].quantile(0.25)
Q3 = df['column'].quantile(0.75)
IQR = Q3 - Q1

lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR

outliers = df[(df['column'] < lower) | (df['column'] > upper)]
```

#### Z-score (for normally distributed data)

```python
from scipy.stats import zscore

df['z_score'] = zscore(df['column'])
outliers = df[df['z_score'].abs() > 3]
```

---

## 🔧 Step 2: Handle Outliers

### ✅ 2.1 Remove Outliers

```python
df_clean = df[(df['column'] >= lower) & (df['column'] <= upper)]
```

### ✅ 2.2 Cap (Winsorization)

```python
from scipy.stats.mstats import winsorize

df['column_winsor'] = winsorize(df['column'], limits=[0.05, 0.05])
```

### ✅ 2.3 Impute Outliers

Replace outliers with mean, median, or a capped value:

```python
df.loc[df['column'] > upper, 'column'] = upper
df.loc[df['column'] < lower, 'column'] = lower
```

---

## ⚙️ Example: IQR Method

```python
import pandas as pd

df = pd.DataFrame({'score': [10, 12, 14, 15, 100, 105, 13, 14, 16]})

Q1 = df['score'].quantile(0.25)
Q3 = df['score'].quantile(0.75)
IQR = Q3 - Q1

lower = Q1 - 1.5 * IQR
upper = Q3 + 1.5 * IQR

df_no_outliers = df[(df['score'] >= lower) & (df['score'] <= upper)]
```

---

## 🧠 Summary

| Method        | When to Use                     |
| ------------- | ------------------------------- |
| Boxplot       | Visual quick check              |
| IQR           | General-purpose for skewed data |
| Z-score       | Normal distributions only       |
| Winsorization | Keep structure, reduce impact   |
| Imputation    | When deletion causes data loss  |

