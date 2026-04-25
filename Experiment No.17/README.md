# Experiment 17 — Statistical and Specialized Data Visualization in Python

## **Name:** Jai Pratp
## **PRN:** 250701231056
## **Branch:** ENTC A3

---

## Aim

To study and implement advanced data visualization techniques — including Heatmaps, Boxplots, Area Plots, and Bubble Charts — for analyzing distributions, detecting outliers, identifying correlations, and representing multi-dimensional data.

---

## Overview

While basic charts communicate simple comparisons, statistical visualization goes further — summarizing complex datasets and surfacing hidden structure that would otherwise go unnoticed. This experiment covers four specialized visualization categories:

- **Distribution & Outlier Detection** — Boxplots and histograms
- **Proportional Breakdown** — Pie and donut charts
- **Correlation Analysis** — Heatmaps to examine inter-variable relationships
- **Multi-dimensional Representation** — Bubble plots encoding several variables at once

---

## Chart Types & When to Use Them

### 1. Area Plot
A filled variant of the line chart where the region beneath the curve is shaded. The shading emphasizes cumulative volume and makes it easier to compare quantities over a shared axis.

> Best for: Tracking Sales vs. Profit over time, visualizing cumulative growth.

---

### 2. Boxplot (Whisker Plot)
Condenses an entire distribution into five descriptive statistics — Minimum, Q1, Median, Q3, and Maximum — displayed as a compact box-and-whisker diagram. Points that fall beyond the whiskers are flagged as outliers.

> Best for: Spotting anomalies, comparing spread across groups, understanding skewness.

---

### 3. Heatmap
Encodes numerical values as color intensity across a grid. Particularly effective when applied to a correlation matrix, where it immediately reveals which variables move together and which are independent.

> Best for: Correlation analysis, feature relationship mapping, confusion matrices.

---

### 4. Bubble Plot
An extension of the scatter plot that encodes a third variable through bubble size and optionally a fourth through color. This allows a two-dimensional plot to carry four dimensions of information simultaneously.

> Best for: Multi-variable comparisons, financial data, demographic analysis.

---

## Key Functions Reference

| Function | Library | Purpose |
|---|---|---|
| `plt.fill_between()` | Matplotlib | Generates area plots |
| `plt.pie()` | Matplotlib | Creates pie and donut charts |
| `plt.Circle()` | Matplotlib | Adds center overlay for donut chart effect |
| `sns.boxplot()` | Seaborn | Visualizes distribution and flags outliers |
| `sns.heatmap()` | Seaborn | Renders color-coded correlation grids |
| `.corr()` | Pandas | Computes pairwise correlation matrix |
| `sns.scatterplot()` | Seaborn | Creates bubble plots with size and hue encoding |

---

## Implementation Highlights

**Correlation Heatmap:**
```python
corr = df[['Age', 'Income', 'Loan_Amount', 'Credit_Score']].corr()
sns.heatmap(corr, annot=True, cmap='coolwarm')
```

**Donut Chart:**
```python
plt.pie(df['Values'], labels=df['Category'], autopct='%1.2f%%')
centre_circle = plt.Circle((0, 0), 0.4, fc='white')
fig = plt.gcf()
fig.gca().add_artist(centre_circle)
```

**Bubble Plot:**
```python
sns.scatterplot(x='Income', y='Loan_Amount', size='Credit_Score',
                hue='Age', data=df, sizes=(50, 500))
```

---

## Dataset Observations

| Technique | Insight Gained |
|---|---|
| **Boxplot** | Reveals extreme or anomalous loan amounts as outliers |
| **Heatmap** | Exposes relationships between income, credit score, and loan amount |
| **Histogram** | Indicates whether a variable is normally distributed or skewed |

---

## Conclusion

Statistical and specialized visualizations move beyond simple comparison charts to reveal the deeper structure of data — its spread, its outliers, its internal correlations, and its multi-dimensional relationships. This experiment demonstrated how heatmaps, boxplots, area plots, and bubble charts each serve a distinct analytical purpose, collectively forming an indispensable toolkit for thorough exploratory data analysis (EDA) in any data science workflow.
