# 💰 Tips Prediction

## Overview
Predicted tip amount based on features like total bill, day, time, party size, and gender using regression.

## Problem Type
Regression — Predicting tip amount in dollars

---

## Dataset
- **Source:** Seaborn built-in dataset
- **Rows:** 244 restaurant records
- **Columns:** 7 (total_bill, tip, sex, smoker, day, time, size)
- **Target:** Tip amount ($)
- **Missing Values:** None

---

## Steps Followed

### 1. Data Exploration
- Checked shape, data types, missing values
- Zero missing values — clean dataset!

### 2. Feature Encoding
Encoded categorical columns to numbers:
- sex, smoker, day, time → numerical values

### 3. Train/Test Split
- 80% training, 20% testing

### 4. Model Training
- Linear Regression

### 5. Evaluation
- MSE, RMSE, R² Score

---

## Results

| Metric | Score |
|--------|-------|
| MSE | 39.41 |
| RMSE | 6.28 |
| R² Score | 0.48 |

---

## Key Findings
- R² of **0.48** means the model explains only 48% of tip variation
- RMSE of **$6.28** — predictions off by $6 on average (significant for small tips!)
- Human tipping behavior is influenced by many **unmeasurable factors** — mood, service quality, personality
- Important lesson: **not every problem is perfectly predictable** from available data
- This is a realistic outcome — real world data science often has limitations!

---

## Technologies Used
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score
```

---

## How to Run
1. Open `Tips_Project.ipynb` in Jupyter Notebook
2. Run **Kernel → Restart & Run All**
3. All outputs will be generated automatically!
