# 📊 Study of NumPy Library in Python

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Library](https://img.shields.io/badge/Library-NumPy-orange.svg)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)
![Experiment](https://img.shields.io/badge/Experiment-8-important.svg)

---

* **Name:** Jai Pratap
* **Class:** EnTC A3
* **PRN:** 25070123056

---

## 🎯 Aim

The objective of this experiment is to study the **NumPy (Numerical Python)** library and understand its role in numerical computations.

This includes:

* Creating arrays
* Performing mathematical operations
* Understanding array properties
* Indexing and slicing
* Statistical and matrix operations

---

## 📘 Introduction

NumPy (Numerical Python) is a powerful Python library used for **numerical and scientific computing**. It supports:

* Multi-dimensional arrays
* Mathematical functions
* Linear algebra operations
* Statistical analysis

Unlike Python lists, NumPy arrays are implemented in **C**, making them:

* ⚡ Faster
* 💾 Memory efficient

---

## 📚 Theory

### 🔹 1. Importing NumPy

```python
import numpy as np
```

---

### 🔹 2. Creating Arrays

```python
arr = np.array([1, 2, 3, 4])
```

---

### 🔹 3. Types of Arrays

```python
# 1D Array
np.array([1, 2, 3])

# 2D Array
np.array([[1, 2], [3, 4]])

# 3D Array
np.array([[[1, 2], [3, 4]]])
```

---

### 🔹 4. Array Attributes

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])

arr.ndim   # Dimensions
arr.shape  # Shape
arr.size   # Total elements
arr.dtype  # Data type
```

---

### 🔹 5. Special Functions

```python
np.zeros((2, 3))
np.ones((2, 3))
np.arange(1, 10)
np.linspace(0, 10, 5)
```

---

### 🔹 6. Indexing & Slicing

```python
# Indexing
arr[0]
arr[1, 2]

# Slicing
arr[0:2]
arr[:, 1]
```

---

### 🔹 7. Mathematical Operations

```python
arr + 5
arr * 2
arr1 + arr2
```

---

### 🔹 8. Statistical Functions

```python
np.sum(arr)
np.mean(arr)
np.median(arr)
np.max(arr)
np.min(arr)
np.std(arr)
```

---

### 🔹 9. Reshaping Arrays

```python
arr.reshape(2, 3)
```

---

### 🔹 10. Matrix Operations

```python
np.dot(arr1, arr2)

# OR
arr1 @ arr2

# Transpose
arr.T
```

---

### 🔹 11. Broadcasting

```python
arr + 10
```

---

## ✅ Advantages of NumPy

* ⚡ Faster than Python lists
* 💾 Memory efficient
* 📊 Supports multi-dimensional arrays
* 🧮 Built-in mathematical functions
* 🔬 Widely used in scientific computing

---

## 🌍 Applications

* Data Science
* Machine Learning
* Scientific Computing
* Financial Analysis
* Signal Processing
* Image Processing

---

## 🏁 Conclusion

NumPy is a **core library for numerical computing in Python**.

This experiment helped in understanding:

* Array creation and manipulation
* Mathematical & statistical operations
* Efficient data handling

👉 It forms the **foundation for advanced libraries** like Pandas and Scikit-learn.

---

## ⭐ Future Scope

* Learn **Pandas for data analysis**
* Explore **Matplotlib for visualization**
* Use NumPy in **Machine Learning projects**

---

## 📌 Repository Info

> 📁 Experiment: 8
> 📦 Library Used: NumPy
> 🧠 Level: Beginner to Intermediate

---
