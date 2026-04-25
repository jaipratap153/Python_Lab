# Experiment 18 — Real-World and Interactive Data Visualizations in Python

## **Name:** Jai Pratap
## **PRN:** 25070123056
## **Branch:** ENTC A3

---

## Aim

To implement advanced and interactive data visualization techniques using Plotly, SciPy, and Matplotlib-Venn for representing hierarchical structures, process flows, set relationships, and multi-dimensional datasets.

---

## Overview

Standard 2D charts are powerful but limited — they struggle to convey hierarchical structure, multi-variable relationships, or dynamic flows within a single view. This experiment moves beyond conventional plots to explore visualization techniques that add depth, interactivity, and narrative to complex data:

- **Interactive visualizations** — Plotly-powered charts with zooming, hovering, and rotation
- **Hierarchical representation** — Treemaps and dendrograms for nested and clustered data
- **Process flow mapping** — Sankey diagrams to track transitions and quantities
- **Set relationships** — Venn diagrams for overlap and intersection analysis

---

## Chart Types & When to Use Them

### 1. Treemap
Encodes hierarchical data as nested rectangles, where each rectangle's area is proportional to its value. Entire category hierarchies can be visualized in a single compact view.

> Best for: Budget allocation, storage distribution, market share breakdowns.

---

### 2. Dendrogram
A branching tree diagram produced by hierarchical clustering algorithms. The height at which branches merge indicates the distance or dissimilarity between clusters.

> Best for: Identifying natural groupings in data, choosing the optimal number of clusters.

---

### 3. Sankey Diagram
A flow diagram where nodes represent stages and the width of connecting bands encodes the volume of flow between them. Makes transitions and proportions immediately legible.

> Best for: Student progression tracking, energy flow analysis, user journey mapping.

---

### 4. Radar (Spider) Chart
Projects multiple variables onto axes radiating from a central point, forming a polygon whose shape encodes the overall profile of an observation.

> Best for: Skill assessments, multi-metric performance comparisons, player statistics.

---

### 5. 3D Scatter Plot
Extends the conventional scatter plot by introducing a third numerical axis, enabling the simultaneous exploration of three-variable relationships within an interactive, rotatable space.

> Best for: Scientific datasets, financial modeling, any analysis involving three continuous variables.

---

## Key Functions Reference

| Function | Library | Purpose |
|---|---|---|
| `px.treemap()` | Plotly Express | Renders nested hierarchical rectangles |
| `px.scatter_3d()` | Plotly Express | Creates interactive 3D scatter plots |
| `go.Sankey()` | Plotly Graph Objects | Builds flow diagrams between stages |
| `go.Scatterpolar()` | Plotly Graph Objects | Generates radar/spider charts |
| `linkage()` | SciPy | Performs hierarchical clustering |
| `dendrogram()` | SciPy | Plots the resulting cluster tree |
| `venn2()` | Matplotlib-Venn | Visualizes intersections between two sets |

---

## Implementation Highlights

**3D Scatter Plot:**
```python
import plotly.express as px

fig = px.scatter_3d(df, x='Study_Hours', y='Marks', z='Attendance',
                    color='Grade', size='Attendance')
fig.show()
```

**Hierarchical Clustering Dendrogram:**
```python
from scipy.cluster.hierarchy import dendrogram, linkage

linked = linkage(data, method='ward')
dendrogram(linked, labels=df['Student'].values)
plt.title('Student Clustering Dendrogram')
plt.show()
```

**Sankey Diagram:**
```python
import plotly.graph_objects as go

fig = go.Figure(go.Sankey(
    node=dict(label=["Enrolled", "Active", "Passed", "Dropped"]),
    link=dict(source=[0, 0, 1, 1], target=[1, 3, 2, 3], value=[80, 20, 65, 15])
))
fig.show()
```

---

## Applications

| Domain | Use Case |
|---|---|
| **Education** | Mapping student progression through course stages via Sankey diagrams |
| **HR Analytics** | Evaluating employee skill profiles using radar charts |
| **Finance** | Visualizing portfolio composition with treemaps |
| **Biology / Research** | Species or sample classification using dendrograms |

---

## Conclusion

Advanced visualization techniques unlock a dimension of insight that traditional charts simply cannot reach. By leveraging Plotly's interactivity, SciPy's clustering capabilities, and specialized chart types like Sankey diagrams and treemaps, this experiment demonstrated how complex, multi-dimensional, and hierarchical data can be communicated with clarity and precision — forming an essential layer of any serious exploratory data analysis workflow.
