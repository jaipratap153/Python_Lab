# Experiment 16 — Data Visualization using Matplotlib and Seaborn

## **Name:** Jai Pratap
## **PRN:** 25070123056
## **Branch:** ENTC A3

---

## Aim

To study and implement data visualization techniques using Matplotlib and Seaborn for representing numerical and categorical data, and to analyze trends, comparisons, distributions, and relationships.

---

## Overview

Data visualization is the graphical representation of data through charts and graphs. It transforms raw numbers into visual stories — making patterns, trends, and outliers immediately apparent rather than buried in rows of data.

**Matplotlib** is a low-level Python plotting library that offers granular control and deep customization over every element of a figure.

**Seaborn** is a high-level library built on top of Matplotlib that produces attractive, statistically informative visualizations with significantly simpler syntax.

---

## Key Concepts

**Visual Encoding** — Representing data values through visual properties like color, size, and position.

**Trend Analysis** — Tracking continuous changes over time using line charts.

**Categorical Comparison** — Contrasting discrete groups using bar charts.

**Distribution Analysis** — Understanding how values are spread using histograms.

**Correlation** — Identifying relationships between two numerical variables using scatter plots.

---

## Chart Types & When to Use Them

### Line Charts — Trend Analysis
Display data points connected by lines to show continuous change over time.

> Best for: Daily study hours, monthly sales figures, time-series data.

---

### Bar Charts — Comparison
Represent categorical data using rectangular bars whose height encodes value.

- **Simple bar chart** — Compares a single variable across categories
- **Grouped bar chart** — Compares multiple variables side by side across categories

> Best for: Comparing marks across days, performance across subjects.

---

### Histograms — Distribution
Group continuous data into bins to show frequency distribution across a range.

> Best for: Understanding how marks or scores are distributed across a class.

The `alpha` parameter controls bar transparency, useful when overlaying multiple histograms.

---

### Scatter Plots — Correlation
Plot two numerical variables against each other to reveal relationships or clusters.

> Best for: Exploring the relationship between study hours and marks, sales vs. profit.

Conditional color encoding can be applied to represent a third categorical variable (e.g., Pass/Fail).

---

## Key Functions Reference

| Function | Library | Description |
|---|---|---|
| `plt.plot()` | Matplotlib | Creates line charts |
| `plt.bar()` | Matplotlib | Creates bar charts |
| `plt.hist()` | Matplotlib | Creates histograms |
| `plt.scatter()` | Matplotlib | Creates scatter plots |
| `plt.legend()` | Matplotlib | Adds a legend to the plot |
| `plt.xticks()` | Matplotlib | Customizes x-axis tick labels |
| `sns.lineplot()` | Seaborn | Aesthetic line plots with confidence intervals |
| `sns.barplot()` | Seaborn | Statistical bar charts with error bars |
| `sns.scatterplot()` | Seaborn | Scatter plots with built-in hue and style options |

---

## Implementation Highlights

**Annotating bar chart values:**
```python
bars = plt.bar(df['Days'], df['Marks'], color='cyan')
for bar in bars:
    plt.text(bar.get_x() + bar.get_width()/2,
             bar.get_height(), str(int(bar.get_height())),
             ha='center', va='bottom')
```

**Grouped bar chart using NumPy offsets:**
```python
x = np.arange(len(df['Days']))
width = 0.35
plt.bar(x - width/2, df['Study_Hours'], width, label='Study Hours')
plt.bar(x + width/2, df['Marks'], width, label='Marks')
```

**Seaborn plots:**
```python
sns.lineplot(x='Day', y='Sales', data=df)
sns.scatterplot(x='Sales', y='Profit', data=df)
```

---

## Applications

| Domain | Use Case |
|---|---|
| Academic Analysis | Comparing study hours against exam marks |
| Business Analysis | Tracking sales and profit trends over time |
| Data Science | Exploratory Data Analysis (EDA) on any dataset |

---

## Conclusion

Data visualization bridges the gap between raw data and human understanding. This experiment demonstrated how Matplotlib provides precise, fine-grained control for building detailed plots, while Seaborn enables fast, visually polished statistical graphics with minimal code. Mastering both libraries equips a data analyst with the tools to communicate insights clearly and effectively across any domain.
