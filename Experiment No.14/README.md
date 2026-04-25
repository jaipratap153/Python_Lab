# Experiment 14 — Data Normalization and Encoding Categorical Variables in Python

#**Name:** Jai Pratap
#**PRN:** 25070123056
#**Branch:** ENTC A3

---

## Aim

To study and perform data normalization and convert categorical variables into quantitative variables using various Python functions and operations.

---

## Theory

Raw data in real-world scenarios is rarely clean or computation-ready. It often contains features that vary wildly in scale, alongside categorical information that mathematical models cannot process directly. Using such data without preprocessing leads to biased results and poor model performance.

Two preprocessing techniques address these problems: **Data Normalization** and **Categorical Variable Encoding**.

---

### 1. Data Normalization

Data normalization rescales numerical features into a common range so that no single feature dominates others due to its magnitude alone.

Consider a dataset with the following features:

| Feature | Range |
|---|---|
| Price | 500 – 50,000 |
| Rating | 1 – 5 |
| Units Sold | 10 – 1,000 |

Without normalization, the large values of Price would overshadow Rating entirely, producing skewed analysis. Normalization levels this playing field.

**Benefits of normalization:**
- Brings all features to a comparable scale
- Prevents high-magnitude features from dominating
- Improves the performance and convergence of machine learning algorithms
- Makes cross-variable comparisons meaningful

---

#### Types of Normalization

**Min-Max Normalization**
Scales all values to a fixed range of 0 to 1 by subtracting the column minimum and dividing by its range. Best used when the data distribution is known and bounded.

> Functions used: `min()`, `max()`

**Z-Score Normalization (Standardization)**
Transforms values based on how far they deviate from the column mean, measured in standard deviations. A result near 0 is close to the mean; positive values are above it, negative values below.

> Functions used: `mean()`, `std()`

**Decimal Scaling**
Scales values by dividing by increasing powers of 10 until all values fall within a small range (typically −1 to 1). Simple and effective for datasets with clearly defined maximum magnitudes.

> Operation used: Division by powers of 10

---

#### Useful Functions for Normalization

| Function | Description |
|---|---|
| `describe()` | Summary statistics — mean, std, min, max, and quartiles |
| `dtypes` | Identifies which columns are numerical and require normalization |
| `loc[]` | Label-based column selection |
| `iloc[]` | Index-based column selection |

---

### 2. Encoding Categorical Variables

Categorical variables hold qualitative labels that cannot be used directly in mathematical models. Common examples include Gender (Male/Female), Payment Method (UPI/Debit Card), and Product Category (Electronics/Clothing).

Since most algorithms require numerical input, categorical data must be converted — a process called **categorical encoding**.

---

#### Encoding Methods

**Label Encoding**
Assigns a unique integer to each category.

| Category | Encoded Value |
|---|---|
| Male | 0 |
| Female | 1 |

Simple and compact, but introduces an implied ordering between categories that may mislead the model.

> Functions used: `LabelEncoder()`, `fit_transform()`

---

**One-Hot Encoding**
Creates a separate binary column for each category, marking presence with 1 and absence with 0.

| Category | Electronics | Clothing | Home |
|---|---|---|---|
| Electronics | 1 | 0 | 0 |
| Clothing | 0 | 1 | 0 |

Eliminates any false ordering between categories and is widely preferred in machine learning.

> Function used: `get_dummies()`

---

**Dummy Encoding**
Identical to One-Hot Encoding, but drops one column to eliminate redundancy and prevent multicollinearity. The dropped category is implicitly represented when all remaining columns are 0.

> Function used: `get_dummies(drop_first=True)`

---

## Conclusion

Data normalization and categorical encoding are two cornerstones of effective data preprocessing. Normalization ensures numerical features contribute equally regardless of their original scale, while encoding makes qualitative variables usable in computational models. Together, these techniques produce cleaner, fairer, and more reliable datasets — directly improving the accuracy and performance of any data analysis or machine learning pipeline.
