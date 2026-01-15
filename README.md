# 💳 Credit Card Fraud Detection using Machine Learning

## 📌 Project Overview
Credit card fraud detection is a real-world machine learning problem where fraudulent transactions are extremely rare compared to legitimate ones.  
The objective of this project is to build robust ML models that can **accurately detect fraud despite severe class imbalance**.

This project demonstrates an **end-to-end data science workflow** including EDA, feature analysis, model training, evaluation, and comparison.

---

## 📊 Dataset Description
- **Total transactions:** 284,807  
- **Fraud cases:** 492 (≈ 0.17%)  
- **Features:** 31 numerical columns  

### Columns:
- `Time` – Seconds elapsed since the first transaction  
- `V1` to `V28` – PCA-transformed features (privacy protected)  
- `Amount` – Transaction amount  
- `Class` – Target variable  
  - `0` → Normal  
  - `1` → Fraud  

✔ No missing values  
✔ Highly imbalanced dataset  

---

## ⚠️ Key Challenge
The dataset is **extremely imbalanced**, making accuracy a misleading metric.  
Therefore, this project focuses on **ROC-AUC and probability-based evaluation**.

---

## 🔍 Exploratory Data Analysis (EDA)
The following analyses were performed:

- Class distribution (bar plot & pie chart)
- Transaction amount distribution (histogram & boxplot)
- Time-based transaction analysis
- Feature correlation heatmap

### Key Insights:
- Fraud transactions account for less than **0.2%**
- Fraud often involves **smaller transaction amounts**
- PCA features show meaningful correlation with fraud patterns

---

## 🧠 Machine Learning Models Used
Multiple models were trained and compared:

- **Random Forest Classifier**
- **AdaBoost Classifier**
- **LightGBM Classifier**

Cross-validation and early stopping were applied to prevent overfitting.

---

## 📈 Evaluation Metrics
Due to class imbalance, the following metrics were used:
- **ROC-AUC Score**
- Out-of-Fold (OOF) predictions
- Cross-validated performance

Accuracy was avoided as the primary metric.

---

## 🏆 Results
| Model | ROC-AUC |
|------|--------|
| Random Forest | ~0.94 |
| AdaBoost | ~0.95 |
| **LightGBM** | **~0.97** |

✅ **LightGBM achieved the best performance**

---

## ⭐ Feature Importance
- Feature importance was extracted from the LightGBM model
- Helped identify the most influential PCA components contributing to fraud detection

---

## 🛠️ Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- LightGBM
- Jupyter Notebook

---

Thank You
