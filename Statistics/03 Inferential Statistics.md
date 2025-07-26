### 📈 Inferential Statistics — Full Overview

**Inferential Statistics** is the branch of statistics that allows you to:

> 🔍 **Draw conclusions about a population** based on a **sample** of data.

It uses **probability theory** to make educated guesses, predictions, and decisions from incomplete data.

---

## 🌳 Branch Hierarchy

```
Inferential Statistics
├── Estimation
│   ├── Point Estimation
│   └── Interval Estimation (Confidence Intervals)
│
├── Hypothesis Testing
│   ├── Null & Alternative Hypotheses
│   ├── Test Statistics (t, z, chi-square)
│   └── p-values & Significance
│
├── Probability Distributions
│   ├── Normal Distribution
│   ├── Binomial, Poisson, etc.
│
└── Regression & Correlation
    ├── Linear Regression
    └── Pearson/Spearman Correlation
```

---

## 🔹 1. Estimation

### a) **Point Estimation**

Provides a **single value** estimate of a population parameter.

> Example:
> Estimate the **average income** of a city from a sample of 500 people.

### b) **Interval Estimation (Confidence Interval)**

Gives a **range** of values likely to include the population parameter.

> Example:
> "We are 95% confident that the average height is between 160–170 cm."

---

## 🔹 2. Hypothesis Testing

Used to test assumptions about a population.

### Key Concepts:

| Term                            | Meaning                                           |
| ------------------------------- | ------------------------------------------------- |
| **Null Hypothesis (H₀)**        | No effect or difference (status quo)              |
| **Alternative Hypothesis (H₁)** | There is an effect or difference                  |
| **p-value**                     | Probability of observing the result if H₀ is true |
| **Significance Level (α)**      | Threshold for rejecting H₀ (usually 0.05)         |

### Example:

* H₀: A new drug is **not** more effective than the old one.
* H₁: The new drug **is** more effective.
* If `p-value < 0.05`, we reject H₀ and conclude the drug works better.

---

## 🔹 3. Probability Distributions

They describe how values are distributed.

| Distribution       | When it's used                             |
| ------------------ | ------------------------------------------ |
| **Normal**         | Bell-shaped, many natural datasets         |
| **Binomial**       | Yes/No outcomes over trials                |
| **Poisson**        | Count of rare events in a fixed time/space |
| **t-distribution** | Small samples, unknown standard deviation  |

---

## 🔹 4. Regression & Correlation

### a) **Correlation**

Measures **strength and direction** of a relationship between variables.

* Pearson: linear correlation (e.g., height & weight)
* Spearman: ranked (ordinal) variables

### b) **Regression**

Predicts the **value of a dependent variable** using one or more independent variables.

> Example: Predicting house price based on area and number of rooms.

---

## 🧪 Real-Life Example

**Problem:**
A company wants to know if **remote work increases productivity**.

**Steps:**

1. Sample 100 remote and 100 office workers.
2. Compute their average output.
3. Use a **t-test** to compare groups.
4. If p-value < 0.05 → conclude remote work boosts productivity.

---

## 🧠 Summary Table

| Topic               | Purpose                                   | Tool / Concept          |
| ------------------- | ----------------------------------------- | ----------------------- |
| Point Estimation    | Single best guess                         | Sample Mean             |
| Confidence Interval | Range where true value lies (with % conf) | 95% CI                  |
| Hypothesis Testing  | Test claims                               | t-test, z-test, p-value |
| Regression          | Predict values                            | Linear regression       |
| Correlation         | Measure relationship strength             | Pearson, Spearman       |

