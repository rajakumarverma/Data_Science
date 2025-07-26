## **1. Hypothesis Testing Basics**

**🎯 Goal:** Check if a guess (hypothesis) is true or not.

**🧠 Concept:**
You start with a guess (**null hypothesis H₀**) and test if it's wrong.

**👩‍🏫 Formula:**

* Start with H₀ (Null Hypothesis): "Nothing is different."
* H₁ (Alternate Hypothesis): "Something is different."
* Collect data ➜ Perform test ➜ Decide to **keep** or **reject** H₀.

**🎉 Example:**
You think your toy car is faster than your friend’s. That’s your H₁.
H₀ says: "Both are equally fast."
You race many times to test it!

---

## **2. P-value in Hypothesis Testing**

**🔍 What it is:** Probability your results happened by **luck** if H₀ is true.

**🧮 Formula:**
P-value = probability of getting your result (or more extreme) if H₀ is true.

**📏 Decision rule:**

* If **P < 0.05**, we reject H₀.
* If **P ≥ 0.05**, we do not reject H₀.

**🎉 Example:**
You flip a coin 10 times and get 9 heads. P-value tells you, "Wow, that’s rare!" Maybe the coin is not fair.

---

## **3. Z-test in Hypothesis Testing**

**🏁 Use when:** You know population standard deviation and sample size is large.

**🧮 Formula:**

$$
Z = \frac{\bar{x} - \mu}{\sigma / \sqrt{n}}
$$

Where:

* $\bar{x}$ = sample mean
* $\mu$ = population mean
* $\sigma$ = population std dev
* $n$ = sample size

**🎉 Example:**
You compare your test score with the average school score using a Z-test.

---

## **4. Student’s t-Distribution**

**🎓 Use when:** Sample size is **small** and you **don’t know** the population std dev.

Looks like a **fatter** version of the normal curve.

**🎉 Example:**
You want to check if your friends in your class (10 kids) are taller than kids in another class.

---

## **5. T-Test and T-Statistics**

**📘 Use when:** Like Z-test, but for **small samples**.

**🧮 Formula:**

$$
t = \frac{\bar{x} - \mu}{s / \sqrt{n}}
$$

Where:

* $s$ = sample standard deviation

**🎉 Example:**
You and your friend eat cookies. You think you eat more. Use T-test to check!

---

## **6. Z-test vs T-test**

| Feature        | Z-test               | T-test         |
| -------------- | -------------------- | -------------- |
| Sample Size    | Large (n > 30)       | Small (n < 30) |
| Std Dev Known? | Yes ($\sigma$ known) | No (use $s$)   |

**🎉 Example:**

* Z-test = Compare many kids' scores (known info).
* T-test = Compare a small group (less info).

---

## **7. Type I and Type II Errors**

**❌ Mistakes:**

* **Type I Error (α):** Rejecting H₀ when it’s true (False Alarm)
* **Type II Error (β):** Not rejecting H₀ when it’s false (Missed it)

**🎉 Example:**

* Type I: Saying cookie jar is empty when it’s not.
* Type II: Saying cookie jar is full when it’s actually empty.

---

## **8. Bayes’ Theorem**

**🔄 Updates belief after getting new info.**

**🧮 Formula:**

$$
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
$$

**🎉 Example:**
You think a toy is in a box (P(A)). You hear it shake (B). You update your belief using Bayes'.

---

## **9. Confidence Interval and Margin of Error**

**🧠 Concept:** We are "pretty sure" the true value lies in a range.

**🧮 Formula (CI):**

$$
\text{CI} = \bar{x} \pm z \cdot \frac{\sigma}{\sqrt{n}}
$$

**Margin of Error =** $z \cdot \frac{\sigma}{\sqrt{n}}$

**🎉 Example:**
You say, "I think I have 10 to 12 marbles." That’s your confidence interval.

---

## **10. Chi-Square Test**

**📦 Use for:** Testing categories.

**🧮 Formula:**

$$
\chi^2 = \sum \frac{(O - E)^2}{E}
$$

Where:

* $O$ = observed count
* $E$ = expected count

**🎉 Example:**
You expect 5 red, 5 green, and 5 blue candies. You got 8 red, 4 green, 3 blue. Is it just luck?

---

## **11. Chi-Square Goodness-of-Fit Test**

**✅ Checks if observed counts match expected counts.**

**🎉 Example:**
If candy colors don’t match what you expect, this test tells you if something’s off.

---

## **12. What is ANOVA**

**🔢 Compare 3 or more groups.**

**🎉 Example:**
Compare how much 3 pets eat: dog, cat, rabbit. Is one group eating way more?

---

## **13. Assumptions of ANOVA**

You need:

1. Groups are **independent**
2. Data is **normally distributed**
3. Groups have **equal variances**

**🎉 Example:**
Different pets should eat independently, and their eating habits should be normal.

---

## **14. Types of ANOVA**

* **One-way ANOVA**: One factor (e.g., pet type)
* **Two-way ANOVA**: Two factors (e.g., pet type + food type)

---

## **15. Partitioning of ANOVA**

**🧮 Formula:**

$$
\text{Total SS} = \text{Between SS} + \text{Within SS}
$$

**🎉 Example:**
You want to know if pet eating differences are **because of pet type** (between) or just **random** (within).

