### 📊 Descriptive Statistics — Complete Overview

**Descriptive Statistics** is the branch of statistics that focuses on **summarizing and describing** the features of a dataset.

It does **not** make predictions or generalizations beyond the data — that's the job of **inferential statistics**.

---

## 🧱 Components of Descriptive Statistics

```
Descriptive Statistics
├── Measures of Central Tendency
├── Measures of Dispersion (Spread)
└── Data Visualization
```

---

## 1️⃣ Measures of Central Tendency

These describe the **center** or **average** of the data.

| Measure    | Description              | Example                  |
| ---------- | ------------------------ | ------------------------ |
| **Mean**   | Average value            | (2+4+6)/3 = 4            |
| **Median** | Middle value when sorted | \[3, 5, 7] → median = 5  |
| **Mode**   | Most frequent value      | \[1, 2, 2, 3] → mode = 2 |

---

## 2️⃣ Measures of Dispersion (Spread)

These show **how spread out** the data values are.

| Measure                       | Description                      | Formula / Example  |
| ----------------------------- | -------------------------------- | ------------------ |
| **Range**                     | Max - Min                        | 10 - 2 = 8         |
| **Variance**                  | Avg squared deviation from mean  | σ² = Σ(x - μ)² / n |
| **Standard Deviation**        | Square root of variance          | √Variance          |
| **IQR (Interquartile Range)** | Spread of the middle 50% of data | Q3 − Q1            |

---

## 3️⃣ Data Visualization

Used to **graphically represent** data.

| Method        | Purpose                               | Example                     |
| ------------- | ------------------------------------- | --------------------------- |
| **Histogram** | Shows distribution of continuous data | Distribution of exam scores |
| **Bar Chart** | Compares categories                   | Sales by product type       |
| **Box Plot**  | Visualizes median, IQR, and outliers  | Distribution of income      |
| **Pie Chart** | Shows proportions                     | Market share by company     |

---

## 🧪 Example: Student Scores

```python
import numpy as np
import pandas as pd

scores = [70, 80, 75, 60, 90, 85, 80]

# Mean
mean = np.mean(scores)

# Median
median = np.median(scores)

# Mode
mode = pd.Series(scores).mode()[0]

# Standard Deviation
std_dev = np.std(scores)

# Range
range_ = max(scores) - min(scores)

print(f"Mean: {mean}, Median: {median}, Mode: {mode}, Std Dev: {std_dev}, Range: {range_}")
```

---

## 🧠 Summary Table

| Concept     | Tells Us                  | Useful For                     |
| ----------- | ------------------------- | ------------------------------ |
| Mean        | Overall average           | Balanced datasets              |
| Median      | Middle value              | Skewed data                    |
| Mode        | Most frequent value       | Categorical or repetitive data |
| Std. Dev    | Spread around the mean    | Consistency or variability     |
| Range / IQR | Total spread / middle 50% | Outlier detection              |

