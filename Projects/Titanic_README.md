# 🚢 Titanic Survival Prediction

## Overview
Predicted survival of Titanic passengers based on features like age, sex, fare, and passenger class using machine learning classification algorithms.

## Problem Type
Binary Classification — Survived (1) or Did Not Survive (0)

---

## Dataset
- **Source:** Seaborn built-in dataset
- **Rows:** 891 passengers
- **Columns:** 15 features
- **Target:** Survived (0 = No, 1 = Yes)

---

## Steps Followed

### 1. Data Exploration
- Checked shape, data types, and missing values
- Found 3 columns with missing values

### 2. Data Cleaning
| Column | Missing | Treatment |
|--------|---------|-----------|
| Age | 177 | Filled with median |
| Embarked | 2 | Filled with mode |
| Deck | 688 | Dropped (too many missing) |

### 3. Feature Selection
Dropped redundant and leaky columns:
- `alive` — data leakage (same as target)
- `who` — redundant with sex and age
- `embark_town` — duplicate of embarked
- `class` — duplicate of pclass
- `adult_male` — redundant with sex and age

### 4. Feature Encoding
| Column | Encoding |
|--------|----------|
| sex | male=0, female=1 |
| embarked | S=0, C=1, Q=2 |
| alone | False=0, True=1 |

### 5. Model Training
- Train/Test Split: 80/20
- Trained Logistic Regression and Random Forest

### 6. Evaluation
- Accuracy, Confusion Matrix, Precision, Recall, F1 Score

---

## Results

| Model | Accuracy |
|-------|----------|
| Logistic Regression | 79.89% |
| **Random Forest** | **83.24%** ✅ |

### Confusion Matrix (Random Forest)
```
[[90  15]
 [21  53]]
```
- 90 correctly predicted deaths
- 53 correctly predicted survivals
- Only 36 wrong predictions out of 179!

### Classification Report (Random Forest)
| Class | Precision | Recall | F1 |
|-------|-----------|--------|----|
| 0 (Died) | 0.81 | 0.86 | 0.83 |
| 1 (Survived) | 0.78 | 0.72 | 0.75 |

---

## Feature Importance
| Feature | Importance |
|---------|------------|
| fare | 28.3% |
| sex | 25.7% |
| age | 25.2% |
| pclass | 8.0% |
| sibsp | 4.3% |
| embarked | 3.4% |
| parch | 3.3% |
| alone | 1.5% |

---

## Key Findings
- **Fare** was the most important feature — expensive tickets meant better cabin location and closer access to lifeboats
- **Women** had much higher survival rates — "women and children first" rule is visible in the data
- **First class** passengers survived significantly more than third class
- **Random Forest beat Logistic Regression** by 3.35% accuracy

---

## Visualizations
- Survived vs Died count plot
- Survival by sex
- Survival by passenger class
- Age distribution by survival
- Feature correlation heatmap

---

## Technologies Used
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.ensemble import RandomForestClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report
```

---

## How to Run
1. Open `Titanic_Project.ipynb` in Jupyter Notebook
2. Run **Kernel → Restart & Run All**
3. All outputs will be generated automatically!
