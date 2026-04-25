---

# Experiment 12 — Data Preprocessing and Handling Missing Values in Python

**Name:** Jai Pratap
**PRN:** 25070123056
**Branch:** ENTC A3

---

## Aim

To understand and apply data preprocessing techniques, and to handle missing values in datasets using various Python functions and operations.

---

## Theory

### What is Data Preprocessing?

Data preprocessing is the process of cleaning, organizing, and transforming raw data into a structured, usable format before analysis or model building.

Real-world data is rarely perfect. It frequently contains errors, inconsistencies, and gaps that can compromise the accuracy of any downstream analysis. Common issues include missing values, incorrect data formats, duplicate records, and irrelevant or noisy entries. Proper preprocessing ensures the data is reliable and ready for analysis or machine learning.

---

### Understanding Missing Values

Missing values are among the most frequent problems encountered in datasets. They arise when no data is recorded for a particular observation, and may appear as `NaN`, `NULL`, blank cells, or special symbols like `?`, `-`, or `NA`. Left unaddressed, missing values can produce incorrect conclusions or runtime errors during analysis.

---

## Key Functions and Operations

### Dataset Inspection

| Operation | Function | Description |
|---|---|---|
| View first rows | `head()` | Quick look at the top of the dataset |
| View last rows | `tail()` | Inspect the end of the dataset |
| Dataset summary | `info()` | Rows, columns, data types, and non-null counts |
| Column data types | `dtypes` | Type of data stored in each column |

### Detecting Missing Values

| Operation | Function | Description |
|---|---|---|
| Identify missing values | `isnull()` | Returns `True` where data is missing |
| Count missing values | `isnull().sum()` | Total missing entries per column |
| Detect non-missing values | `notnull()` | Returns `True` where data is present |
| Replace missing symbols | `replace()` | Converts symbols like `?` or `-` to standard `NaN` |

---

## Handling Missing Values

### Removal Strategies

**Drop missing rows** — `dropna()`
Removes any row containing at least one missing value. Best suited when missing data is a very small fraction of the overall dataset.

**Drop missing columns** — `dropna(axis=1)`
Removes entire columns that contain missing values. Appropriate when a column is too sparse to be useful.

### Imputation Strategies

| Method | Functions | Best Used When |
|---|---|---|
| Fill with a fixed value | `fillna(value)` | A known default exists |
| Fill with **mean** | `mean()` + `fillna()` | Data is roughly normally distributed |
| Fill with **median** | `median()` + `fillna()` | Data contains outliers |
| Fill with **mode** | `mode()` + `fillna()` | Data is categorical |
| **Forward fill** | `fillna(method='ffill')` | Previous value is a reasonable estimate |
| **Backward fill** | `fillna(method='bfill')` | Next value is a reasonable estimate |

---

## Other Preprocessing Operations

| Operation | Function | Description |
|---|---|---|
| Remove duplicates | `drop_duplicates()` | Eliminates repeated rows |
| Count unique values | `nunique()` | Number of distinct values in a column |
| List unique values | `unique()` | Displays all distinct categories or entries |

---

## Conclusion

Data preprocessing is a foundational step in any data analysis or machine learning pipeline. Ensuring the dataset is clean, consistent, and complete directly determines the quality and reliability of results. Python's Pandas library provides a comprehensive suite of functions to handle missing values, remove inconsistencies, and prepare data efficiently — making it an essential tool for any data practitioner.
