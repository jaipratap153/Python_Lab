Here's a rewritten version of the readme:

---

# Experiment 11 — Categorical Data Analysis using Python

**Name:** Jai Pratap
**PRN:** 25070123056
**Branch:** ENTC A3

---

## Aim

To analyze categorical data using Python by identifying categories, computing frequency distributions, performing cross-tabulation, and visualizing categorical variables effectively.

---

## Theory

### What is Categorical Data?

Categorical data represents information grouped into distinct labels or classes rather than measured numerically. It answers questions like *"what type?"* or *"which group?"* — not *"how much?"*

Common examples include Gender, Product Category, Payment Method, and Customer Type. This kind of data appears extensively in business analytics, surveys, and market research.

---

### Types of Categorical Data

**Nominal Data** consists of unordered categories with no inherent ranking. One category is not greater or better than another — they are simply labels.

> Examples: Department (IT, CSE, Mechanical), Blood Group (A, B, AB, O), City (Mumbai, Pune, Delhi)

**Ordinal Data** consists of categories that follow a meaningful sequence or ranking, though the gap between levels cannot be precisely measured.

> Examples: Satisfaction (Poor < Average < Good < Excellent), Education (Diploma < Graduate < Postgraduate)

---

### Why Analyze Categorical Data?

Categorical data analysis converts raw qualitative information into actionable insights. It helps to understand how data is distributed across groups, detect patterns in customer behavior, identify relationships between variables, and support data-driven decision making.

Typical questions it answers: *Which product category sells most? Which payment method do customers prefer? How does customer type vary by city?*

---

### Core Operations

| Operation | Description | Python Method |
|---|---|---|
| **Frequency Count** | Count occurrences of each category | `value_counts()` |
| **Unique Categories** | List all distinct categories present | `unique()` |
| **Cross-Tabulation** | Examine relationships between two categorical variables | `pd.crosstab()` |
| **Grouping** | Summarize data and aggregate by category | `groupby()` |

---

### Python Libraries Used

| Library | Purpose |
|---|---|
| **Pandas** | Data manipulation and analysis |
| **Matplotlib** | Basic plotting and visualization |
| **Seaborn** | Advanced statistical visualization |

---

## Conclusion

Categorical data analysis is fundamental to making sense of qualitative information. Through frequency counts, cross-tabulations, and grouping, hidden patterns and relationships within data can be surfaced clearly. Python's ecosystem — particularly Pandas, Matplotlib, and Seaborn — makes this process efficient and scalable, forming an indispensable part of any data analyst's toolkit.
