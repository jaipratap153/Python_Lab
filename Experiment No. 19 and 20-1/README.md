# Experiments 19 & 20 — COVID-19 Intelligence & Global Trends Analysis

## **Name:** Jai Pratap
## **PRN:** 25070123056
## **Branch:** ENTC A3

---

## Aim

To perform a comprehensive Exploratory Data Analysis (EDA) on a global COVID-19 dataset using Python, uncovering infection trends, reporting anomalies, healthcare outcomes, and regional hotspots through data cleaning, feature engineering, and advanced visualization.

---

## Overview

This project applies Python-based data science techniques to a multi-dimensional COVID-19 time-series dataset spanning **January 2020 to May 2021**. The analysis moves through the full EDA pipeline — from raw data cleaning to interactive geospatial mapping — with the goal of transforming messy pandemic records into actionable epidemiological insight.

The study addresses three core questions:
- How did COVID-19 spread and evolve globally over time?
- Where do inconsistencies in national reporting distort the picture?
- Which regions carried the heaviest burden relative to their healthcare capacity?

---

## Tools & Technologies

| Category | Tools | Primary Use |
|---|---|---|
| Data Processing | Pandas, NumPy | Cleaning, aggregation, transformation |
| Static Visualization | Matplotlib, Seaborn | Trend charts, heatmaps, distributions |
| Interactive Mapping | Plotly Express | Choropleth maps, interactive plots |
| Platform | Jupyter Notebook / Google Colab | Execution and visualization environment |

---

## Project Objectives

### 1. Data Cleaning & Preparation
Removed redundant columns (`SNo`, `Last Update`) and converted date fields to proper `datetime` format to enable accurate time-series operations. Missing values were handled and numerical columns were validated for type consistency.

### 2. Feature Engineering
Derived three analytical metrics that do not exist in the raw data but are essential for meaningful cross-country comparison:

| Metric | Description |
|---|---|
| **Active Cases** | Confirmed − Recovered − Deaths |
| **Mortality Rate (%)** | (Deaths / Confirmed) × 100 |
| **Recovery Rate (%)** | (Recovered / Confirmed) × 100 |

### 3. Trend Smoothing
Applied **7-day rolling averages** to daily case counts to eliminate reporting artifacts such as weekend delays and retrospective batch corrections, revealing the true underlying trajectory of the pandemic.

### 4. Geospatial Analysis
Built interactive choropleth maps using Plotly Express to visualize the global distribution of confirmed cases, deaths, and recovery rates — making regional disparities immediately visible.

### 5. Hotspot Identification
Conducted province-level analysis on Spain using `groupby()` and `idxmax()` to pinpoint the highest-burden regions, supported by choropleth mapping for spatial context.

---

## Methodology & Key Findings

### Global Trend Analysis *(Experiment 19)*
- Filtered the dataset to the latest available snapshot (May 29, 2021)
- Aggregated country-level totals using `groupby()` for confirmed cases, deaths, and recoveries
- Generated global distribution charts to identify the most affected nations

**Notable Findings:**

| Observation | Detail |
|---|---|
| Reporting Anomaly | The United States recorded a **0% recovery rate** — not due to actual outcomes, but because the US stopped reporting recoveries partway through the pandemic |
| Wave Detection | India's devastating **second wave peak in April 2021** was clearly identified after applying rolling average smoothing |
| Correlation Study | Heatmap analysis revealed a **~0.95 correlation** between confirmed cases and deaths, while also showing that mortality rate depends more heavily on healthcare system quality than raw case count |

---

### Spain Regional Analysis *(Experiment 20)*
- Disaggregated national data to the province level
- Used `groupby()` aggregation and `idxmax()` to identify the highest-burden provinces
- Visualized regional hotspots on an interactive choropleth map to support targeted analysis

---

## Key Functions Reference

| Function | Library | Purpose |
|---|---|---|
| `.info()`, `.head()` | Pandas | Initial dataset inspection |
| `pd.to_datetime()` | Pandas | Date field conversion |
| `groupby()` | Pandas | Country and region-level aggregation |
| `rolling(7).mean()` | Pandas | 7-day trend smoothing |
| `idxmax()` | Pandas | Locating peak values and hotspots |
| `sns.heatmap()` | Seaborn | Correlation matrix visualization |
| `px.choropleth()` | Plotly Express | Interactive global and regional maps |

---

## Conclusion

This project demonstrates the full power of Python's data science ecosystem applied to a real-world public health crisis. Through systematic cleaning, thoughtful feature engineering, and layered visualization, raw pandemic records were transformed into a coherent analytical narrative — exposing wave patterns, correcting for reporting distortions, and pinpointing regional disparities. The techniques applied here extend well beyond COVID-19 and represent a transferable framework for any large-scale time-series EDA task.
