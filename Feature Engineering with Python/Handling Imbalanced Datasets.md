### ⚖️ Handling Imbalanced Datasets in Python (for Classification Problems)

An **imbalanced dataset** occurs when the number of samples in one class is **much higher or lower** than the other(s), leading to **biased models**.

For example, 95% "No" vs. 5% "Yes" in a churn dataset.

---

## 🔍 Step 1: Detect Imbalance

```python
df['target'].value_counts()
```

---

## 🔧 Step 2: Techniques to Handle Imbalance

### ✅ 1. **Resampling Techniques**

#### 🔹 **Undersampling** – reduce the majority class

```python
from imblearn.under_sampling import RandomUnderSampler

rus = RandomUnderSampler()
X_res, y_res = rus.fit_resample(X, y)
```

#### 🔹 **Oversampling** – increase the minority class

```python
from imblearn.over_sampling import RandomOverSampler

ros = RandomOverSampler()
X_res, y_res = ros.fit_resample(X, y)
```

#### 🔹 **SMOTE (Synthetic Minority Oversampling Technique)**

```python
from imblearn.over_sampling import SMOTE

smote = SMOTE()
X_res, y_res = smote.fit_resample(X, y)
```

---

### ✅ 2. **Class Weights in Models**

Let the model pay more attention to the minority class.

#### Example: Logistic Regression

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression(class_weight='balanced')
model.fit(X_train, y_train)
```

Other models like `RandomForest`, `SVM`, and `XGBoost` also support `class_weight`.

---

### ✅ 3. **Change the Evaluation Metric**

Don't use accuracy for imbalanced data. Use:

| Metric           | Usage                                    |
| ---------------- | ---------------------------------------- |
| Precision/Recall | Useful when one class is more important  |
| F1 Score         | Harmonic mean of precision and recall    |
| ROC AUC          | Classifier's ability to separate classes |
| PR AUC           | Best when positive class is rare         |
| Confusion Matrix | Visualizes TP, FP, FN, TN                |

```python
from sklearn.metrics import classification_report, confusion_matrix

y_pred = model.predict(X_test)
print(classification_report(y_test, y_pred))
print(confusion_matrix(y_test, y_pred))
```

---

### ✅ 4. **Use Ensemble Methods**

* **Balanced Random Forest**
* **EasyEnsemble / BalancedBaggingClassifier** (from `imblearn.ensemble`)
* XGBoost with `scale_pos_weight` parameter

```python
from xgboost import XGBClassifier

model = XGBClassifier(scale_pos_weight=ratio)
```

---

## 📌 Summary of Techniques

| Technique        | Goal                          |
| ---------------- | ----------------------------- |
| Undersampling    | Reduce majority class         |
| Oversampling     | Duplicate/synthesize minority |
| SMOTE            | Create synthetic samples      |
| Class weights    | Penalize majority errors      |
| Metric tuning    | Focus on F1, recall, etc.     |
| Ensemble methods | Improve robustness            |

