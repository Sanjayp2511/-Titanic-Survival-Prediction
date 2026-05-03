# 🛍️ Mall Customer Segmentation

## Overview
Segmented 200 mall customers into meaningful groups based on annual income and spending score using unsupervised machine learning clustering algorithms — with no predefined labels!

## Problem Type
Unsupervised Learning — Clustering

---

## Dataset
- **Source:** Mall Customers Dataset
- **Rows:** 200 customers
- **Columns:** 5 (CustomerID, Genre, Age, Annual Income, Spending Score)
- **Target:** None — unsupervised learning!
- **Missing Values:** None

---

## Steps Followed

### 1. Data Exploration
- Checked shape, data types, missing values
- Zero missing values — clean dataset!

### 2. Feature Selection
Selected 2 most informative features:
- **Annual Income (k$)** — how much customer earns
- **Spending Score (1-100)** — how much customer spends

### 3. Data Scaling
- Applied StandardScaler to normalize features
- Important for clustering — prevents income ($) from dominating spending score (1-100)

### 4. Finding Optimal K (Elbow Method)
- Ran K-Means for K=1 to K=10
- Plotted inertia vs number of clusters
- Elbow found at **K=5** — optimal number of clusters!

### 5. Training 3 Clustering Algorithms
- K-Means
- Hierarchical (Agglomerative)
- DBSCAN

### 6. Visual Comparison
- Side by side scatter plots of all 3 algorithms

---

## Results

| Algorithm | Clusters Found | Notes |
|-----------|---------------|-------|
| **K-Means** | **5** ✅ | Best result — clear segments |
| Hierarchical | 5 | Similar to K-Means |
| DBSCAN | 2 + 8 outliers | Density based, fewer clusters |

---

## Customer Segments (K-Means)

| Cluster | Income | Spending | Customer Type |
|---------|--------|----------|---------------|
| 🔵 Cluster 1 | High | High | Luxury Shoppers 💎 |
| 🟢 Cluster 2 | Low | High | Impulsive Buyers 🛍️ |
| 🟣 Cluster 3 | High | Low | Careful Savers 💰 |
| 🟠 Cluster 4 | Low | Low | Budget Shoppers 🪙 |
| 🔴 Cluster 0 | Medium | Medium | Average Shoppers 🛒 |

---

## Key Findings
- **Elbow method** confirmed 5 as the optimal number of clusters
- **K-Means** produced the clearest and most actionable customer segments
- **DBSCAN** identified 8 outlier customers who don't fit any group
- **Hierarchical clustering** confirmed the same 5 groups as K-Means
- Results provide **actionable business intelligence** for targeted marketing strategies

## Business Applications
- Target **Luxury Shoppers** with premium brand promotions
- Target **Impulsive Buyers** with buy-now-pay-later offers
- Target **Careful Savers** with quality and value messaging
- Target **Budget Shoppers** with discount deals and offers

---

## Visualizations
- Elbow method chart
- K-Means scatter plot with 5 color-coded clusters
- Hierarchical dendrogram
- Side-by-side comparison of all 3 algorithms

---

## Technologies Used
```python
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans, DBSCAN, AgglomerativeClustering
from sklearn.preprocessing import StandardScaler
import scipy.cluster.hierarchy as sch
```

---

## How to Run
1. Open `Clustering_Project.ipynb` in Jupyter Notebook
2. Run **Kernel → Restart & Run All**
3. All outputs will be generated automatically!
