# 🧠 Data Science Projects Portfolio

> A collection of end-to-end data science projects covering classification, regression, clustering, and exploratory data analysis — built using Python and popular ML libraries.

**Author:** Sanjay P  
**Tools:** Python | Pandas | NumPy | Scikit-learn | XGBoost | Seaborn | Matplotlib  

---

## 📁 Projects Overview

| # | Project | Type | Dataset | Best Score |
|---|---------|------|---------|------------|
| 1 | 🚢 Titanic Survival Prediction | Classification | Titanic | 83.24% accuracy |
| 2 | ✈️ Flight Passenger Prediction | Regression | Flights | 0.95 R² score |
| 3 | 🌸 Iris Flower Classification | Multi-class Classification | Iris | 100% accuracy |
| 4 | 🐧 Penguin Species Classification | Multi-class Classification | Penguins | - |
| 5 | 💰 Tips Prediction | Regression | Tips | - |
| 6 | 🛍️ Mall Customer Segmentation | Clustering | Mall Customers | 5 segments |

---

## 🚢 Project 1 — Titanic Survival Prediction

### Overview
Predicted survival of Titanic passengers based on features like age, sex, fare, and passenger class.

### Problem Type
Binary Classification — Survived (1) or Did Not Survive (0)

### Steps Followed
- Data loading and exploration
- Missing value treatment (median for age, mode for embarked)
- Feature engineering and encoding
- Model training and comparison
- Evaluation using accuracy, confusion matrix, precision, recall

### Models Used & Results
| Model | Accuracy |
|-------|----------|
| Logistic Regression | 79.89% |
| Random Forest | **83.24%** ✅ |

### Key Findings
- Fare was the most important feature (28.3% importance)
- Sex was 2nd most important — women had much higher survival rates
- First class passengers survived significantly more than third class
- Random Forest outperformed Logistic Regression by 3.35%

### Technologies
`Python` `Pandas` `Scikit-learn` `Seaborn` `Matplotlib`

---

## ✈️ Project 2 — Flight Passenger Prediction

### Overview
Predicted the number of airline passengers based on year and month using historical flight data from 1949-1960.

### Problem Type
Regression — Predicting a continuous number (passenger count)

### Steps Followed
- Data loading and exploration
- Month name encoding (Jan=1, Feb=2... Dec=12)
- Train/test split
- Model training
- Evaluation using MAE, RMSE, R² score

### Models Used & Results
| Model | MAE | RMSE | R² Score |
|-------|-----|------|----------|
| Random Forest Regressor | 17.95 | 21.82 | **0.95** ✅ |

### Key Findings
- Year was the most important feature (87.6%) — consistent passenger growth every year
- Month contributed 12.4% — seasonal summer peaks (May-August)
- Strong upward trend in air travel from 1949 to 1960
- Clear seasonality — passenger numbers peak in summer months

### Technologies
`Python` `Pandas` `Scikit-learn` `Seaborn` `Matplotlib`

---

## 🌸 Project 3 — Iris Flower Classification

### Overview
Classified iris flowers into three species (Setosa, Versicolor, Virginica) based on petal and sepal measurements.

### Problem Type
Multi-class Classification — 3 flower species

### Steps Followed
- Data loading (clean dataset, no missing values)
- Train/test split
- Training and comparing 7 different ML models
- Evaluation and model comparison

### Models Used & Results
| Model | Accuracy |
|-------|----------|
| Logistic Regression | 100.00% |
| SVM | 100.00% |
| Naive Bayes | 100.00% |
| Decision Tree | 97.78% |
| KNN | 97.78% |
| XGBoost | 97.78% |
| Random Forest | 93.33% |

### Key Findings
- Iris is a clean, well-separated dataset — simple models achieve perfect accuracy
- More complex models don't always win — Logistic Regression tied with SVM at 100%
- Random Forest scored lowest due to randomness on small clean datasets

### Technologies
`Python` `Pandas` `Scikit-learn` `XGBoost` `Seaborn` `Matplotlib`

---

## 🐧 Project 4 — Penguin Species Classification

### Overview
Classified penguin species based on physical measurements like bill length, bill depth, flipper length, and body mass.

### Problem Type
Multi-class Classification — 3 penguin species

### Technologies
`Python` `Pandas` `Scikit-learn` `Seaborn` `Matplotlib`

---

## 💰 Project 5 — Tips Prediction

### Overview
Predicted tip amount based on features like total bill, day, time, party size, and gender.

### Problem Type
Regression — Predicting tip amount in dollars

### Models Used & Results
| Model | RMSE | R² Score |
|-------|------|----------|
| Linear Regression | 6.28 | 0.48 |

### Key Findings
- R² of 0.48 shows tip amount is hard to predict purely from available features
- Human tipping behavior is influenced by many unmeasurable factors (mood, service quality)
- Good lesson — not every problem is perfectly predictable from available data!

### Technologies
`Python` `Pandas` `Scikit-learn` `Seaborn` `Matplotlib`

---

## 🛍️ Project 6 — Mall Customer Segmentation

### Overview
Segmented 200 mall customers into meaningful groups based on annual income and spending score — without any predefined labels. Pure unsupervised learning!

### Problem Type
Unsupervised Learning — Clustering

### Steps Followed
- Data loading and exploration
- Feature selection (Annual Income, Spending Score)
- Data scaling using StandardScaler
- Elbow method to find optimal K
- Training and comparing 3 clustering algorithms
- Visual comparison of all algorithms

### Models Used & Results
| Algorithm | Clusters Found | Notes |
|-----------|---------------|-------|
| K-Means | 5 | Best result — clear segments |
| Hierarchical | 5 | Similar to K-Means |
| DBSCAN | 2 + 8 outliers | Density based, fewer clusters |

### Customer Segments Found (K-Means)
| Cluster | Income | Spending | Type |
|---------|--------|----------|------|
| 🔵 Cluster 1 | High | High | Luxury Shoppers 💎 |
| 🟢 Cluster 2 | Low | High | Impulsive Buyers 🛍️ |
| 🟣 Cluster 3 | High | Low | Careful Savers 💰 |
| 🟠 Cluster 4 | Low | Low | Budget Shoppers 🪙 |
| 🔴 Cluster 0 | Medium | Medium | Average Shoppers 🛒 |

### Key Findings
- Elbow method confirmed 5 as optimal number of clusters
- K-Means produced the clearest customer segments
- DBSCAN identified 8 outlier customers who don't fit any group
- Results provide actionable business intelligence for targeted marketing

### Technologies
`Python` `Pandas` `Scikit-learn` `Seaborn` `Matplotlib` `SciPy`

---

## 🛠️ Tech Stack

```python
# Core Libraries
import pandas as pd          # Data manipulation
import numpy as np           # Numerical computing
import matplotlib.pyplot as plt  # Visualization
import seaborn as sns        # Statistical visualization

# Machine Learning
from sklearn.linear_model import LogisticRegression, LinearRegression
from sklearn.ensemble import RandomForestClassifier, RandomForestRegressor
from sklearn.tree import DecisionTreeClassifier
from sklearn.neighbors import KNeighborsClassifier
from sklearn.svm import SVC
from sklearn.naive_bayes import GaussianNB
from sklearn.cluster import KMeans, DBSCAN, AgglomerativeClustering
from xgboost import XGBClassifier
```

---

## 📊 Skills Demonstrated

- ✅ Data Cleaning & Preprocessing
- ✅ Exploratory Data Analysis (EDA)
- ✅ Feature Engineering & Selection
- ✅ Supervised Learning (Classification & Regression)
- ✅ Unsupervised Learning (Clustering)
- ✅ Model Evaluation & Comparison
- ✅ Data Visualization
- ✅ Hyperparameter Awareness

---

## 🚀 How to Run

1. Clone the repository
```bash
git clone https://github.com/Sanjayp2511/-Titanic-Survival-Prediction.git
```

2. Install required libraries
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy
```

3. Open Jupyter Notebook
```bash
jupyter notebook
```

4. Navigate to the `Projects` folder and open any project!

---

## 📬 Connect With Me

- **GitHub:** [Sanjayp2511](https://github.com/Sanjayp2511)

---

*Built with curiosity, persistence, and a lot of ☕*
