# ✈️ Flight Passenger Prediction

## Overview
Predicted the number of airline passengers based on year and month using historical flight data from 1949 to 1960.

## Problem Type
Regression — Predicting a continuous number (passenger count)

---

## Dataset
- **Source:** Seaborn built-in dataset
- **Rows:** 144 records (12 months × 12 years)
- **Columns:** 3 (year, month, passengers)
- **Target:** Number of passengers

---

## Steps Followed

### 1. Data Exploration
- Checked shape, data types, missing values
- Zero missing values — clean dataset!

### 2. Feature Engineering
- Encoded month names to numbers (Jan=1, Feb=2... Dec=12)
- Preserving natural order of months is important for time series data

### 3. Model Training
- Train/Test Split: 80/20 (random_state=7)
- Trained Random Forest Regressor with 150 trees

### 4. Evaluation
- MAE, MSE, RMSE, R² Score

---

## Results

| Metric | Score |
|--------|-------|
| MAE | 17.95 passengers |
| MSE | 475.99 |
| RMSE | 21.82 passengers |
| **R² Score** | **0.95** ✅ |

### What This Means
- On average predictions are off by only **~18 passengers**
- Model explains **95% of the variation** in passenger numbers
- Excellent result for a simple 2-feature model!

---

## Feature Importance
| Feature | Importance |
|---------|------------|
| year | 87.6% |
| month | 12.4% |

---

## Key Findings
- **Year** dominates at 87.6% — consistent passenger growth every year as air travel became more affordable
- **Month** contributes 12.4% — seasonal summer peaks (May-August)
- Clear **upward trend** from 1949 to 1960
- Clear **seasonality** — passengers always peak in summer months
- Two simple features (year, month) achieved 0.95 R² — shows how predictable historical air travel growth was

---

## Visualizations
- Actual vs Predicted passengers line chart
- Passenger growth over years
- Seasonal passenger pattern by month
- Feature importance bar chart

---

## Technologies Used
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_squared_error, r2_score, mean_absolute_error
```

---

## How to Run
1. Open `Flights_Project.ipynb` in Jupyter Notebook
2. Run **Kernel → Restart & Run All**
3. All outputs will be generated automatically!
