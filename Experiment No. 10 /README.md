---

## 👨‍🎓 Student Details

* **Name:** Jai Pratap
* **Class:** EnTC A3
* **PRN:** 25070123056

---

## 🎯 Aim

The aim of this experiment is to create a dataset using Python and perform basic data inspection operations such as checking size, shape, structure, and statistical summaries using the Pandas library.

---

## 🎯 Objectives

* 📌 Create a dataset using a Python dictionary
* 📌 Convert the dataset into a Pandas DataFrame
* 📌 Save and load data using CSV files
* 📌 Perform data inspection using built-in Pandas functions

---

## 💻 Software Requirements

* Python 3.x
* Pandas Library
* Jupyter Notebook / Google Colab / Python IDE

---

## 📘 Theory

A dataset is a structured collection of related data. In Pandas, datasets are represented using **DataFrames**, which are two-dimensional tables with labeled rows and columns, similar to spreadsheets.

Datasets can be:

* Created manually in code
* Imported from external files like CSV, Excel, JSON, or databases

After loading a dataset, it is important to analyze its structure, check for missing values, and understand the data types. Pandas provides built-in functions that make this process simple and efficient.

---

## 🔍 Basic Inspection Functions

| Function        | Description                           |
| --------------- | ------------------------------------- |
| `df.shape`      | Returns number of rows and columns    |
| `df.size`       | Returns total elements                |
| `df.info()`     | Displays structure and data types     |
| `df.describe()` | Statistical summary of numerical data |
| `df.head()`     | First 5 rows                          |
| `df.tail()`     | Last 5 rows                           |
| `df.columns`    | List of column names                  |

---

## 🧪 Program

### 🔹 Part A: Creating the Dataset

```python
import pandas as pd

data = {
    "Roll_No": [101, 102, 103, 104, 105],
    "Name": ["Amit", "Neha", "Rohit", "Sneha", "Kiran"],
    "Marks": [85, 90, 78, 88, 76],
    "Department": ["IT", "CS", "IT", "ENTC", "CS"]
}

df = pd.DataFrame(data)
print(df)
```

---

### 🔹 Part B: Dataset Inspection

```python
print("Shape:", df.shape)
print("Size:", df.size)

print("\nColumn Names:\n", df.columns)
print("\nFirst 5 rows:\n", df.head())
print("\nLast 5 rows:\n", df.tail())

print("\nDataset Info:\n")
df.info()

print("\nStatistical Summary:\n", df.describe())
```

---

### 🔹 Part C: Saving Dataset to CSV

```python
df.to_csv("students.csv", index=False)
```

---

### 🔹 Part D: Reading Dataset from CSV

```python
df2 = pd.read_csv("students.csv")
print("\nUploaded Dataset:\n", df2)
```

---

## 📌 Output

* ✅ Dataset created and displayed successfully
* ✅ Shape: **(5, 4)** and Size: **20**
* ✅ Column names displayed correctly
* ✅ `info()` confirmed correct data types and no missing values
* ✅ `describe()` generated statistical summary
* ✅ CSV file saved and loaded successfully

---

## 🚀 Key Features

* 📊 Easy dataset creation
* 🔍 Quick data inspection tools
* 💾 Efficient file handling (CSV)
* ⚡ Fast and reliable data operations

---

## 🌍 Applications

* Data Analysis
* Data Cleaning
* Machine Learning Preprocessing
* Business Analytics
* Research and Statistics

---

## 🏁 Conclusion

This experiment demonstrated how to create a dataset using Python and Pandas, inspect it using built-in functions, and save/load it using CSV files.

These operations form the **foundation of real-world data analysis workflows** and are essential for working with data in fields like data science and machine learning.

---
