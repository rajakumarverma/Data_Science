
# 🔹 1. **What is NumPy in Pandas?**

Pandas uses **NumPy arrays** internally to store data. Most operations on Pandas `Series` and `DataFrame` objects rely on NumPy functions.

* `pandas.Series` = 1D labeled array (built on top of `numpy.ndarray`)
* `pandas.DataFrame` = 2D labeled array (uses NumPy internally)

---

# 🔹 2. **Using NumPy Functions in Pandas**

You can directly apply NumPy functions to Pandas objects because they are essentially wrappers around NumPy arrays.

---

## ✅ Example Dataset Setup

```python
import pandas as pd
import numpy as np

data = pd.DataFrame({
    'A': [10, 20, np.nan, 40, 50],
    'B': [5, np.nan, 15, 20, 25],
    'C': [100, 200, 300, 400, 500]
})
print(data)
```

### Output:

```
      A     B    C
0  10.0   5.0  100
1  20.0   NaN  200
2   NaN  15.0  300
3  40.0  20.0  400
4  50.0  25.0  500
```

---

# 🔹 3. **Popular NumPy Functions Used in Pandas**

---

## ✅ `np.mean()` — Mean of a column

```python
np.mean(data['A'])
```

### Output:

```
30.0
```

---

## ✅ `np.median()` — Median

```python
np.median(data['A'].dropna())
```

### Output:

```
30.0
```

---

## ✅ `np.std()` — Standard Deviation

```python
np.std(data['A'].dropna())
```

### Output:

```
15.811388300841896
```

---

## ✅ `np.sum()` — Sum of values

```python
np.sum(data['C'])
```

### Output:

```
1500
```

---

## ✅ `np.isnan()` — Find NaNs

```python
np.isnan(data['A'])
```

### Output:

```
0    False
1    False
2     True
3    False
4    False
Name: A, dtype: bool
```

---

## ✅ `np.where()` — Conditional replacement

```python
data['A_clean'] = np.where(np.isnan(data['A']), 0, data['A'])
print(data)
```

### Output:

```
      A     B    C  A_clean
0  10.0   5.0  100     10.0
1  20.0   NaN  200     20.0
2   NaN  15.0  300      0.0
3  40.0  20.0  400     40.0
4  50.0  25.0  500     50.0
```

---

## ✅ `np.round()` — Rounding

```python
np.round(data['C'] / 3, 2)
```

### Output:

```
0     33.33
1     66.67
2    100.00
3    133.33
4    166.67
Name: C, dtype: float64
```

---

## ✅ `np.log()`, `np.sqrt()`, `np.exp()` — Mathematical functions

```python
np.sqrt(data['C'])
```

### Output:

```
0    10.000000
1    14.142136
2    17.320508
3    20.000000
4    22.360680
Name: C, dtype: float64
```

---

## ✅ `np.clip()` — Limit values to a range

```python
np.clip(data['C'], 150, 400)
```

### Output:

```
0    150
1    200
2    300
3    400
4    400
Name: C, dtype: int64
```

---

## ✅ `np.argsort()` — Indices to sort

```python
data['A'].argsort()
```

### Output:

```
0    0
1    1
2    4
3    2
4    3
Name: A, dtype: int64
```

---

## ✅ `np.percentile()` — Percentile values

```python
np.percentile(data['A'].dropna(), 50)  # median
```

### Output:

```
30.0
```

---

## ✅ `np.corrcoef()` — Correlation between columns

```python
np.corrcoef(data['A'].fillna(0), data['C'])
```

### Output:

```
array([[1.        , 0.97780241],
       [0.97780241, 1.        ]])
```

---

## ✅ `np.unique()` — Unique values

```python
np.unique(data['C'])
```

### Output:

```
array([100, 200, 300, 400, 500])
```

---

## ✅ `np.diff()` — Difference between consecutive elements

```python
np.diff(data['C'])
```

### Output:

```
array([100, 100, 100, 100])
```

---

## ✅ `np.isnan().sum()` — Count missing values

```python
np.isnan(data['A']).sum()
```

### Output:

```
1
```

---

# 🔹 4. **Using NumPy Arrays Directly to Create Pandas Objects**

```python
array = np.array([[1, 2], [3, 4]])
df = pd.DataFrame(array, columns=['X', 'Y'])
print(df)
```

### Output:

```
   X  Y
0  1  2
1  3  4
```

---

# 🔹 5. **Broadcasting with NumPy in Pandas**

```python
data['C_scaled'] = data['C'] / np.array([10])
print(data[['C', 'C_scaled']])
```

### Output:

```
     C  C_scaled
0  100      10.0
1  200      20.0
2  300      30.0
3  400      40.0
4  500      50.0
```

---

# 🔹 6. **NumPy with Apply Functions**

```python
data['A_squared'] = data['A'].apply(np.square)
print(data[['A', 'A_squared']])
```

### Output:

```
      A  A_squared
0  10.0      100.0
1  20.0      400.0
2   NaN        NaN
3  40.0     1600.0
4  50.0     2500.0
```

---

# 🔹 Summary Table of Common NumPy Functions Used in Pandas

| NumPy Function                  | Purpose                 | Pandas Use                 |
| ------------------------------- | ----------------------- | -------------------------- |
| `np.mean()`                     | Mean                    | Series/column stats        |
| `np.std()`                      | Standard deviation      | Analysis                   |
| `np.isnan()`                    | Check missing values    | Data cleaning              |
| `np.where()`                    | Conditional assignment  | Replace NaN or apply logic |
| `np.round()`                    | Rounding numbers        | Presentation               |
| `np.clip()`                     | Limit values            | Outlier control            |
| `np.unique()`                   | Unique values           | Analysis                   |
| `np.percentile()`               | Percentiles             | Descriptive stats          |
| `np.corrcoef()`                 | Correlation             | Bivariate analysis         |
| `np.diff()`                     | Difference between rows | Time series                |
| `np.sqrt(), np.log(), np.exp()` | Math operations         | Transformations            |

