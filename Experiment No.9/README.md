---

# **Jai Pratap**

**EnTC A3 | PRN: 250701231056**

## **Experiment – 9: Study of Pandas Library in Python**

---

## **Aim**

The objective of this experiment is to learn about the Pandas library in Python and understand its use in data handling and analysis. This includes creating Series and DataFrames, importing and exporting data files, selecting and filtering datasets, managing missing values, performing statistical calculations, and organizing data through grouping and sorting.

---

## **Introduction**

Pandas is one of the most essential Python libraries used for data analysis and manipulation. It introduces two key data structures — the **Series** (for one-dimensional data) and the **DataFrame** (for two-dimensional tabular data) — which simplify working with structured datasets.

Built on top of NumPy, Pandas combines efficient numerical computation with powerful features like labeling, indexing, and file handling. It is widely used in fields such as data science, machine learning, finance, and business analytics. Whether working with small datasets or large CSV files and database outputs, Pandas handles them efficiently.

---

## **Theory**

### **Importing Pandas**

Pandas is typically imported using a standard alias to keep the code short and readable:

```python
import pandas as pd
```

This `pd` alias is universally used in almost all Python data-related projects.

---

### **Pandas Series**

A Series is a one-dimensional labeled array capable of storing different data types such as integers, strings, or floats. It can be compared to a single column in a spreadsheet, where each value has a corresponding index.

```python
import pandas as pd

data = pd.Series([10, 20, 30, 40])
print(data)
```

By default, the index starts from 0, but custom labels can also be assigned:

```python
pd.Series([10, 20, 30], index=["a", "b", "c"])
```

This allows accessing values using meaningful labels instead of positions.

---

### **Pandas DataFrame**

A DataFrame is a two-dimensional data structure organized in rows and columns, similar to an Excel sheet or database table.

```python
data = {
    "Name": ["A", "B", "C"],
    "Marks": [85, 90, 88]
}

df = pd.DataFrame(data)
print(df)
```

Each column in a DataFrame behaves like a Series, meaning Series operations apply within DataFrames as well.

---

### **Reading Data from CSV Files**

In practical scenarios, data is usually imported from files. Pandas allows this with a simple command:

```python
df = pd.read_csv("file.csv")
```

Useful functions for exploring the dataset include:

* `df.head()` – displays first 5 rows
* `df.tail()` – displays last 5 rows
* `df.info()` – shows dataset summary
* `df.describe()` – gives statistical details

---

### **Data Selection and Indexing**

Pandas provides different methods for selecting data:

* **Using labels (loc):**

```python
df.loc[0]
```

* **Using positions (iloc):**

```python
df.iloc[0]
```

Selecting columns:

```python
df["Marks"]
df[["Name", "Marks"]]
```

---

### **Filtering Data**

Filtering helps extract rows that meet specific conditions:

```python
df[df["Marks"] > 85]
```

Multiple conditions can be combined using `&` (and) or `|` (or).

---

### **Handling Missing Values**

Real-world datasets often contain missing values. Pandas provides functions to manage them:

* `df.isnull()` – identifies missing values
* `df.notnull()` – identifies valid values
* `df.dropna()` – removes missing data
* `df.fillna()` – replaces missing values

Example:

```python
df.fillna(0)
```

---

### **Sorting Data**

Sorting data in a DataFrame is simple:

```python
df.sort_values("Marks")
```

Sorting by multiple columns:

```python
df.sort_values(["Marks", "Name"])
```

Descending order can be achieved using `ascending=False`.

---

### **GroupBy Operations**

The `groupby()` function is a powerful feature used to group data and perform operations on each group:

```python
df.groupby("Department").mean()
```

This calculates the average values for each department.

---

### **Descriptive Statistics**

Pandas includes built-in statistical functions:

* `df.mean()` – average
* `df.sum()` – total
* `df.min()` / `df.max()` – smallest/largest
* `df.count()` – non-null values
* `df.std()` – standard deviation

Example:

```python
df["Marks"].mean()
```

---

## **Advantages of Pandas**

* Simplifies data handling and analysis
* Provides powerful data manipulation tools
* Efficiently handles large datasets
* Works well with NumPy and Matplotlib
* Essential for data science tasks

---

## **Disadvantages**

* Requires installation as an external library
* Can consume more memory for large datasets
* Slightly difficult for beginners, especially indexing concepts

---

## **Tools Used**

* Python Interpreter
* Jupyter Notebook
* VS Code / IDLE
* Pandas Library

---

## **Applications**

Pandas is widely used in:

* Data cleaning
* Exploratory data analysis
* Financial analysis
* Business reporting
* Machine learning preprocessing
* Research and statistics

---

## **Conclusion**

Pandas is a powerful and essential library for working with data in Python. In this experiment, we learned how to create Series and DataFrames, load data from files, filter and manipulate datasets, handle missing values, and perform statistical analysis efficiently.

Understanding Pandas acts as a bridge between basic Python programming and advanced fields like data science, machine learning, and analytics, where it is extensively used.

---
