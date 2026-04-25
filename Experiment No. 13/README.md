# Experiment 13 — Data Binning and Data Formatting in Python

**Name:** Jai Pratap
**PRN:** 25070123056
**Branch:** ENTC A3

---

## Aim

To understand and perform data binning and data formatting using Python tools and functions.

---

## Theory

In real-world data analysis, raw data is often messy and unorganized. Before it can be analyzed properly, it must be cleaned and structured — a process known as data preprocessing. Two essential techniques within preprocessing are **data binning** and **data formatting**.

---

### 1. Data Binning

Data binning is the process of grouping continuous numerical values into discrete categories or ranges called bins. Rather than working with exact values, data is divided into meaningful segments that are easier to interpret and analyze.

**Why use binning?**
- Reduces noise and minor fluctuations in data
- Makes underlying patterns more visible
- Converts continuous data into categorical form for further analysis

**Example — Age Binning:**

| Age | Category |
|-----|----------|
| 18  | Young    |
| 30  | Adult    |
| 60  | Senior   |

Instead of analyzing every individual age, values are grouped into intuitive categories.

---

### 2. Data Formatting

Data formatting involves converting data into a consistent, standardized structure so it can be processed and analyzed accurately. Inconsistent formats are a common source of errors in data pipelines.

**Common formatting tasks include:**
- Converting text strings into numeric types
- Standardizing date formats
- Normalizing text case (uppercase/lowercase)
- Removing unwanted whitespace or special characters

Proper formatting improves data accuracy, readability, and consistency.

---

## Functions Reference

### Data Binning

| Function | Description |
|---|---|
| `pd.cut()` | Divides data into equal-width intervals |
| `pd.qcut()` | Divides data into quantile-based bins with equal observations per bin |
| `value_counts()` | Counts how many values fall into each bin |
| `labels` parameter | Assigns custom names to bins such as Low, Medium, or High |

### Data Formatting

| Function | Description |
|---|---|
| `dtypes` | Inspects the data type of each column |
| `astype()` | Converts a column from one data type to another |
| `pd.to_numeric()` | Converts string-encoded numbers into proper numeric types |
| `pd.to_datetime()` | Parses and converts data into a standard datetime format |
| `str.lower()` | Converts all text to lowercase |
| `str.upper()` | Converts all text to uppercase |
| `str.title()` | Capitalizes the first letter of each word |
| `str.strip()` | Removes leading and trailing whitespace |
| `replace()` | Corrects or standardizes inconsistent values |

---

## Conclusion

Data binning and formatting are fundamental preprocessing steps that bring structure and consistency to raw datasets. Binning simplifies complex continuous data into interpretable categories, while formatting ensures all values follow a uniform, analysis-ready structure. Together, these techniques improve data quality, reduce errors, and lay a solid foundation for accurate and reliable analysis.
