# Fraud Detection using Machine Learning (IEEE-CIS Dataset)

## 📌 Project Overview
This project focuses on building a machine learning system to detect fraudulent transactions using the IEEE-CIS Fraud Detection dataset. The dataset is highly imbalanced, making it a realistic and challenging fraud detection problem.

The main objective is to develop a model that effectively balances **fraud detection (recall)** and **false positive control (precision)**.

---

## 📊 Dataset
- Source: IEEE-CIS Fraud Detection (Kaggle)
- Type: Transactional data
- Key challenge: Highly imbalanced classes (fraud vs non-fraud)

---

## ⚙️ Approach

### 1. Data Preprocessing
- Dropped useless columns(which contained high null values and their missingness was also not informative)
- Handled missing values(used heuristic-based approach to decide how to fill the missing values)
- Encoded categorical variables using one-hot encoding and frequency encoding based on cardinality.
- Scaled numerical features where necessary
- Addressed class imbalance using weighting techniques

---

### 2. Models Tried
- Logistic Regression
- Logistic Regression (class-weighted)
- Random Forest
- XGBoost
- LightGBM

---

## 🏆 Final Model Selection

After extensive experimentation, **LightGBM** was selected as the final model due to its superior balance between precision and recall after threshold tuning.

### Final LightGBM Performance
- Precision: ~0.50
- Recall: ~0.75
- F1 Score: ~0.60
- ROC-AUC: ~0.95

---

## 🎯 Key Technique: Threshold Tuning
Instead of relying on the default 0.5 probability threshold, the decision boundary was optimized to achieve a target recall, significantly improving fraud detection performance while maintaining acceptable precision.

---

## 📈 Key Insights
- Fraud detection is a **precision–recall tradeoff problem**, not just an accuracy problem.
- Adjusting classification thresholds can significantly improve real-world performance.
- LightGBM outperformed other models in terms of overall balance and stability.

---

## 🔮 Future Improvements
- Advanced feature engineering (temporal + behavioral features)
- Hyperparameter optimization using Bayesian methods (Optuna)
- Model ensembling for further performance gains
- Feature importance analysis using SHAP

---

## 🛠️ Tech Stack
- Python
- Pandas, NumPy
- Scikit-learn
- LightGBM
- XGBoost
- Matplotlib

---
