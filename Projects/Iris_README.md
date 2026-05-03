# 🌸 Iris Flower Classification

## Overview
Classified iris flowers into three species based on petal and sepal measurements. Compared 7 different machine learning models to find the best performer.

## Problem Type
Multi-class Classification — 3 flower species (Setosa, Versicolor, Virginica)

---

## Dataset
- **Source:** Seaborn built-in dataset
- **Rows:** 150 flowers
- **Columns:** 5 (sepal_length, sepal_width, petal_length, petal_width, species)
- **Target:** Species (setosa, versicolor, virginica)
- **Missing Values:** None — perfectly clean dataset!

---

## Steps Followed

### 1. Data Exploration
- Checked shape, data types, missing values
- Zero missing values — no cleaning needed!

### 2. Train/Test Split
- 80% training, 20% testing
- random_state=42 for reproducibility

### 3. Model Training & Comparison
Trained 7 different classification models and compared results

### 4. Evaluation
- Accuracy Score
- Classification Report (Precision, Recall, F1)

---

## Results — Model Comparison

| Model | Accuracy |
|-------|----------|
| Logistic Regression | 100.00% 🏆 |
| SVM | 100.00% 🏆 |
| Naive Bayes | 100.00% 🏆 |
| Decision Tree | 97.78% |
| KNN | 97.78% |
| XGBoost | 97.78% |
| Random Forest | 93.33% |

---

## Key Findings
- **3 models achieved perfect 100% accuracy** — Iris is a very clean, well-separated dataset
- **Simple models won** — Logistic Regression performed as well as complex XGBoost
- **Random Forest scored lowest** — randomness hurts on small, clean datasets
- Important lesson: **more complex ≠ always better**!
- Iris flower species have very clear boundaries — even simple algorithms can separate them perfectly

---

## Technologies Used
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.neighbors import KNeighborsClassifier
from sklearn.svm import SVC
from sklearn.naive_bayes import GaussianNB
from xgboost import XGBClassifier
from sklearn.metrics import accuracy_score, classification_report
```

---

## How to Run
1. Open `Iris_project.ipynb` in Jupyter Notebook
2. Run **Kernel → Restart & Run All**
3. All outputs will be generated automatically!
