### **Statistics : Key Concepts & Techniques**
---
Statistics is the branch of mathematics that deals with collecting, organizing, analyzing, interpreting, and presenting data. It helps us make sense of large amounts of information and draw conclusions or make decisions based on that data.
---

### **1. Types of Statistics**

**Introduction:**  
Statistics can be broadly categorized into two types:

- **Descriptive Statistics**: Organizes, summarizes, and simplifies data for better understanding.
- **Inferential Statistics**: Makes inferences or predictions about a population based on sample data.

#### **Descriptive Statistics**  
- **Measures of Central Tendency**: Mean, Median, Mode
- **Measures of Dispersion**: Range, Variance, Standard Deviation
- **Data Visualization**: Histograms, Box Plots, Probability Distribution Functions (PDF), Probability Mass Function (PMF)

#### **Inferential Statistics**  
- **Hypothesis Testing**: Null & Alternate Hypothesis
- **P-Value**: Measures the significance of test results
- **Confidence Interval**: A range of values estimating population parameters
- **Statistical Tests**: Z-test, T-test, ANOVA, Chi-Square Test, F-test

---

### **2. Population vs Sample Data**

**Introduction:**  
Understanding the difference between **population data** (complete set) and **sample data** (subset).

#### **Population Data**  
- **Definition**: Entire set of individuals or objects of interest in a study.
- **Examples**: All students in a school, all consumers in a city.
- **Characteristics**: Complete set, summarized by parameters (mean, variance).

#### **Sample Data**  
- **Definition**: A subset of the population used to represent the whole.
- **Examples**: 100 students randomly selected from a school.
- **Characteristics**: Subset, summarized by statistics (sample mean, sample variance).

---

### **3. Types of Sampling Techniques**

**Introduction:**  
Sampling is essential for making inferences about populations when it's impractical to study the entire population.

#### **Probability Sampling**  
- **Simple Random Sampling**: Every member has an equal chance.
- **Systematic Sampling**: Select every nth member.
- **Stratified Sampling**: Population divided into groups, random samples taken from each group.
- **Cluster Sampling**: Divide into clusters, select entire clusters randomly.
- **Multi-stage Sampling**: Combination of several sampling techniques.

#### **Non-Probability Sampling**  
- **Convenience Sampling**: Data collected from easy-to-reach individuals.
- **Judgmental Sampling**: Researcher selects based on their judgment.
- **Snowball Sampling**: Existing subjects refer others.
- **Quota Sampling**: Select samples based on specific characteristics (e.g., age, gender).

---

### **4. Types of Data**

**Introduction:**  
Understanding the types of data helps in performing the correct statistical analysis.

#### **Quantitative Data**  
- **Discrete Data**: Whole numbers, countable (e.g., number of students).
- **Continuous Data**: Can take any value (e.g., height, weight).

#### **Qualitative Data**  
- **Nominal Data**: Categories without order (e.g., gender, color).
- **Ordinal Data**: Categories with a defined rank (e.g., education level, customer satisfaction).

---

### **5. Scales of Measurement**

**Introduction:**  
Scales of measurement define the nature of data and guide proper statistical analysis.

#### **1. Nominal Scale**
- **Definition**: Categorizes data without any inherent order.
- **Characteristics**: Labels or names, no ranking.
- **Examples**: Gender (Male, Female), Colors (Red, Blue, Green).
- **Application**: Counting frequencies of categories (e.g., number of males and females in a survey).

#### **2. Ordinal Scale**
- **Definition**: Categorizes and ranks data.
- **Characteristics**: Ranked categories, unequal intervals.
- **Examples**: Education Level (High School, Bachelor’s, Master’s), Customer Satisfaction (Poor, Neutral, Excellent).
- **Application**: Rank-based analysis (e.g., customer satisfaction rankings).

#### **3. Interval Scale**
- **Definition**: Ordered data with meaningful differences between intervals, but no true zero.
- **Characteristics**: Equal intervals, no true zero.
- **Examples**: Temperature (°C or °F), IQ Scores, Calendar Years.
- **Application**: Measuring differences but not ratios (e.g., 10°F is 10 degrees warmer than 0°F, but 0°F doesn’t mean "no temperature").

#### **4. Ratio Scale**
- **Definition**: Similar to interval scale but with a true zero.
- **Characteristics**: Ordered data, equal intervals, true zero, allows ratios.
- **Examples**: Weight (kg), Height (cm), Income ($).
- **Application**: Calculating meaningful ratios (e.g., a person weighing 80 kg is twice as heavy as one weighing 40 kg).

---

### **Key Takeaways**

- **Types of Statistics**: Descriptive (summarizes data) vs Inferential (makes inferences about a population).
- **Population vs Sample**: Population is the entire set, sample is a subset.
- **Sampling Techniques**: Probability (random) vs Non-probability (judgmental or convenience).
- **Types of Data**: Quantitative (Discrete and Continuous) vs Qualitative (Nominal and Ordinal).
- **Scales of Measurement**: Nominal (categorical, no order), Ordinal (ranked, unequal intervals), Interval (ordered, equal intervals, no true zero), Ratio (ordered, equal intervals, true zero).

---

### **Quick Reference: Scales of Measurement**

| **Scale**            | **Description**                                                                 | **Examples**                           | **Key Property**                          |
|----------------------|---------------------------------------------------------------------------------|----------------------------------------|--------------------------------------------|
| **Nominal**          | Categorizes data without order.                                                  | Gender, Colors, Religion              | No inherent ranking                        |
| **Ordinal**          | Categorizes and ranks data, but intervals are not necessarily equal.            | Education level, Customer satisfaction | Ranking with unequal intervals             |
| **Interval**         | Data ordered with equal intervals but lacks a true zero point.                  | Temperature (°C, °F), IQ Scores        | Equal intervals, no true zero             |
| **Ratio**            | Similar to interval but with a true zero point.                                | Weight, Height, Income                | Equal intervals, meaningful ratios         |

---

### 🌳 **Complete Tree Hierarchy of Statistics**

```
Statistics
├── 1. Descriptive Statistics
│   ├── 1.1 Measures of Central Tendency
│   │   ├── Mean — (e.g., Average income of employees)
│   │   ├── Median — (e.g., Median house price in a city)
│   │   └── Mode — (e.g., Most common shoe size sold)
│   ├── 1.2 Measures of Dispersion
│   │   ├── Range — (e.g., Max–min temperatures this week)
│   │   ├── Variance — (e.g., Variability in monthly sales)
│   │   ├── Standard Deviation — (e.g., Spread of student marks)
│   │   └── Interquartile Range (IQR) — (e.g., Salary spread)
│   ├── 1.3 Measures of Position
│   │   ├── Percentiles — (e.g., 90th percentile in exam)
│   │   └── Quartiles — (e.g., Q1 and Q3 of earnings data)
│   └── 1.4 Data Visualization
│       ├── Histogram — (e.g., Age distribution of users)
│       ├── Bar Chart — (e.g., Sales per product category)
│       ├── Pie Chart — (e.g., Market share of brands)
│       ├── Boxplot — (e.g., Compare incomes across regions)
│       └── Line Graph — (e.g., Stock prices over time)

├── 2. Inferential Statistics
│   ├── 2.1 Estimation
│   │   ├── Point Estimation — (e.g., Estimate average height)
│   │   └── Confidence Interval — (e.g., 95% CI of blood pressure)
│   ├── 2.2 Hypothesis Testing
│   │   ├── z-test — (e.g., Known population SD, large sample)
│   │   ├── t-test — (e.g., Compare test scores of two classes)
│   │   ├── ANOVA — (e.g., Compare 3 diets for weight loss)
│   │   ├── Chi-square Test — (e.g., Gender vs. brand preference)
│   │   └── p-value — (e.g., p < 0.05 = statistically significant)
│   ├── 2.3 Correlation and Regression
│   │   ├── Pearson/Spearman Correlation — (e.g., Hours studied vs. score)
│   │   └── Linear Regression
│   │       ├── Simple — (e.g., Predict sales from ad budget)
│   │       └── Multiple — (e.g., Predict house price from size & location)
│   ├── 2.4 Probability Distributions
│   │   ├── Discrete Distributions
│   │   │   ├── Binomial — (e.g., 3 heads in 5 coin tosses)
│   │   │   └── Poisson — (e.g., Calls per hour at call center)
│   │   └── Continuous Distributions
│   │       ├── Normal — (e.g., Human height)
│   │       ├── t-distribution — (e.g., Small sample mean estimation)
│   │       ├── Exponential — (e.g., Time between arrivals)
│   │       └── Uniform — (e.g., Random number between 0–1)
│   ├── 2.5 Nonparametric Tests
│   │   ├── Mann-Whitney U test — (e.g., Compare satisfaction between 2 groups)
│   │   ├── Kruskal-Wallis test — (e.g., Compare ranks in 3+ groups)
│   │   └── Wilcoxon signed-rank test — (e.g., Before/after symptom scores)
│   └── 2.6 Bayesian Statistics
│       ├── Prior Distribution — (e.g., Prior disease risk)
│       ├── Posterior Distribution — (e.g., Updated risk after test result)
│       └── Bayes’ Theorem — (e.g., Conditional probability in diagnosis)
```

---
