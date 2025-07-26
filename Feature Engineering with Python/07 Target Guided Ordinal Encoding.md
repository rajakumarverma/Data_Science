### 🎯 Target Guided Ordinal Encoding in Python

**Target Guided Ordinal Encoding** assigns numerical values to categories **based on the relationship with the target variable** — often using the **mean of the target** for each category.

---

## 📌 Why Use It?

* Captures the **impact of categorical features** on the target.
* Useful for models that can leverage ordered relationships (e.g. tree-based models).
* Better than random or alphabetical ordinal mappings.

---

## ✅ Example Scenario

Suppose you have a `City` column and a binary target `Purchased`:

```python
import pandas as pd

df = pd.DataFrame({
    'City': ['London', 'Paris', 'London', 'Berlin', 'Paris', 'Berlin', 'London'],
    'Purchased': [1, 0, 1, 0, 1, 0, 1]
})
```

---

## 🔧 Step-by-Step: Target Guided Ordinal Encoding

### Step 1: Compute mean target per category

```python
mean_target = df.groupby('City')['Purchased'].mean().sort_values()
print(mean_target)
```

**Output:**

```
City
Berlin    0.000
Paris     0.500
London    1.000
```

### Step 2: Map categories to ordered numbers

```python
ordinal_map = {k: i for i, k in enumerate(mean_target.index)}
df['City_encoded'] = df['City'].map(ordinal_map)
```

**Result:**

```
     City  Purchased  City_encoded
0  London          1             2
1   Paris          0             1
2  London          1             2
3  Berlin          0             0
4   Paris          1             1
5  Berlin          0             0
6  London          1             2
```

Now `City` is encoded based on how likely a customer from that city is to purchase.

---

## 🧠 Why It Works

This method encodes:

* **Information gain** about the target
* Maintains **ordinal relationship** between categories based on their predictive strength

It often **boosts performance** for models like:

* Decision Trees
* Random Forest
* XGBoost
* LightGBM

---

## ⚠️ Caution

* Should only be applied on **training data** to avoid data leakage.
* For test/validation, **apply the same mapping** without recalculating means.

---

## 🔄 Wrap as a Reusable Function

```python
def target_guided_ordinal_encoding(df, feature, target):
    means = df.groupby(feature)[target].mean().sort_values()
    mapping = {k: i for i, k in enumerate(means.index)}
    return df[feature].map(mapping), mapping
```
