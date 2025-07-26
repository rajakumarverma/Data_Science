# 🐼 **Pandas in Python – Deep Explanation with Code and Outputs**

---

## 📌 What is Pandas?

**Pandas** is an open-source Python library used for:

* Data manipulation
* Data analysis
* Reading/writing data
* Handling missing data
* Time series analysis

It provides two primary data structures:

* `Series`: 1-dimensional labeled array
* `DataFrame`: 2-dimensional labeled data structure (like an Excel table or SQL table)

---

## 🔧 Installation

```bash
pip install pandas
```

---

## 1️⃣ **Series – 1D Labeled Array**

```python
import pandas as pd

# Creating a Series from a list
data = [10, 20, 30, 40]
series = pd.Series(data)
print(series)
```

### 🔸 Output:

```
0    10
1    20
2    30
3    40
dtype: int64
```

### 🔹 Explanation:

* `0, 1, 2, 3` → **index**
* `10, 20, 30, 40` → **values**

---

### ✅ Custom Index

```python
series = pd.Series(data, index=['a', 'b', 'c', 'd'])
print(series)
```

#### 🔸 Output:

```
a    10
b    20
c    30
d    40
dtype: int64
```

---

### ✅ Series from a dictionary

```python
data_dict = {'math': 90, 'science': 85, 'english': 75}
series = pd.Series(data_dict)
print(series)
```

#### 🔸 Output:

```
math       90
science    85
english    75
dtype: int64
```

---

## 2️⃣ **DataFrame – 2D Table**

### 📌 Create DataFrame from Dictionary

```python
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'City': ['NYC', 'LA', 'Chicago']
}

df = pd.DataFrame(data)
print(df)
```

#### 🔸 Output:

```
      Name  Age     City
0    Alice   25      NYC
1      Bob   30       LA
2  Charlie   35  Chicago
```

---

### ✅ Accessing Columns

```python
print(df['Name'])
```

#### 🔸 Output:

```
0      Alice
1        Bob
2    Charlie
Name: Name, dtype: object
```

---

### ✅ Accessing Rows (by index)

```python
print(df.loc[0])   # by label
print(df.iloc[1])  # by position
```

#### 🔸 Output:

```
Name    Alice
Age         25
City      NYC
Name: 0, dtype: object
```

---

## 🔍 Basic Operations

### ✅ Adding New Column

```python
df['Salary'] = [50000, 60000, 70000]
print(df)
```

#### 🔸 Output:

```
      Name  Age     City  Salary
0    Alice   25      NYC   50000
1      Bob   30       LA   60000
2  Charlie   35  Chicago   70000
```

---

### ✅ Filtering Rows

```python
print(df[df['Age'] > 28])
```

#### 🔸 Output:

```
      Name  Age     City  Salary
1      Bob   30       LA   60000
2  Charlie   35  Chicago   70000
```

---

### ✅ Summary Statistics

```python
print(df.describe())
```

#### 🔸 Output:

```
             Age        Salary
count   3.000000      3.000000
mean   30.000000  60000.000000
std     5.000000  10000.000000
min    25.000000  50000.000000
25%    27.500000  55000.000000
50%    30.000000  60000.000000
75%    32.500000  65000.000000
max    35.000000  70000.000000
```

---

## 📄 Reading and Writing Files

### ✅ CSV

```python
# Reading CSV
df = pd.read_csv('data.csv')

# Writing to CSV
df.to_csv('output.csv', index=False)
```

---

## 🔄 Handling Missing Values

```python
data = {
    'A': [1, 2, None],
    'B': [4, None, 6]
}

df = pd.DataFrame(data)
print(df)
```

### 🔸 Output:

```
     A    B
0  1.0  4.0
1  2.0  NaN
2  NaN  6.0
```

### ✅ Fill Missing Values

```python
print(df.fillna(0))
```

### ✅ Drop Missing Rows

```python
print(df.dropna())
```

---

## 🔄 DataFrame Operations

### ✅ Sorting

```python
print(df.sort_values('A'))
```

### ✅ Group By

```python
data = {
    'Department': ['HR', 'IT', 'HR', 'IT'],
    'Salary': [40000, 60000, 45000, 65000]
}
df = pd.DataFrame(data)
print(df.groupby('Department').mean())
```

#### 🔸 Output:

```
             Salary
Department         
HR           42500.0
IT           62500.0
```

---

## 🕒 Time Series

```python
dates = pd.date_range('2025-01-01', periods=3)
df = pd.DataFrame({'value': [1, 2, 3]}, index=dates)
print(df)
```

---

## 🔄 Merge / Join / Concat

```python
df1 = pd.DataFrame({'ID': [1, 2], 'Name': ['A', 'B']})
df2 = pd.DataFrame({'ID': [1, 2], 'Score': [90, 95]})

merged = pd.merge(df1, df2, on='ID')
print(merged)
```

#### 🔸 Output:

```
   ID Name  Score
0   1    A     90
1   2    B     95
```

---

## 📊 Visualization (optional, if using Matplotlib)

```python
import matplotlib.pyplot as plt

df = pd.DataFrame({'x': [1, 2, 3], 'y': [4, 5, 6]})
df.plot(x='x', y='y', kind='line')
plt.show()
```

---

## 🧠 Summary Table of Key Methods

| Function                | Purpose                    |
| ----------------------- | -------------------------- |
| `read_csv()`            | Load data from CSV file    |
| `to_csv()`              | Save DataFrame to CSV      |
| `head()` / `tail()`     | Preview first/last N rows  |
| `info()`                | DataFrame structure        |
| `describe()`            | Summary statistics         |
| `dropna()` / `fillna()` | Handle missing data        |
| `sort_values()`         | Sort rows                  |
| `groupby()`             | Group data                 |
| `merge()` / `concat()`  | Combine data               |
| `apply()`               | Apply function to elements |

