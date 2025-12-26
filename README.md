# Fraud Detection for E-commerce and Banking Transactions

## Overview

This project develops a fraud detection system for e-commerce and bank credit card transactions. The goal is to accurately identify fraudulent activities while balancing security and customer experience. The work was completed as part of a data science challenge at Adey Innovations Inc.

---

## Objectives

- Clean and preprocess transaction data
- Perform exploratory data analysis (EDA)
- Engineer meaningful time-based and behavioral features
- Integrate geolocation data using IP address mapping
- Handle severe class imbalance
- Prepare datasets for machine learning models

---

## Datasets

- Fraud_Data.csv: E-commerce transaction data
- IpAddress_to_Country.csv: IP-to-country mapping data
- creditcard.csv: Bank transaction data with anonymized features

Target variable:

- class / Class (1 = Fraud, 0 = Non-Fraud)

---

## Project Structure

fraud-detection/
├── data/
│ ├── raw/
│ └── processed/
├── notebooks/
│ └── data_analysis_and_preprocessing.ipynb
├── requirements.txt
└── README.md

---

## Task 1: Data Analysis and Preprocessing

- Data cleaning: handled missing values, removed duplicates, corrected data types
- EDA: univariate, bivariate, and class imbalance analysis
- Geolocation integration: range-based IP-to-country merging and fraud rate analysis
- Feature engineering:
  - hour_of_day, day_of_week
  - time_since_signup
  - transaction frequency and velocity features
- Data transformation:
  - Feature scaling using StandardScaler
  - One-Hot Encoding for categorical features
- Class imbalance handling:
  - Applied SMOTE on training data only
  - Documented class distribution before and after resampling

---

## Tools Used

- Python
- Pandas, NumPy
- Scikit-learn
- Imbalanced-learn
- Matplotlib, Seaborn
- Jupyter Notebook
- Git & GitHub

---

---

## Task 2: Model Building and Training

- Built and evaluated machine learning models to detect fraudulent transactions.
- **Baseline model**: Logistic Regression with `class_weight="balanced"` for handling class imbalance.
- **Ensemble model**: Random Forest with hyperparameter tuning (`n_estimators`, `max_depth`) to improve performance.
- **Evaluation metrics**:
  - **F1-Score** – balances precision and recall, suitable for imbalanced data.
  - **AUC-PR (Average Precision)** – measures model performance for rare events like fraud.
  - **Confusion Matrix** – visual inspection of correct/incorrect predictions.
- **Stratified train-test split** used to preserve the class distribution.
- **Cross-validation (StratifiedKFold, k=5)** applied to estimate reliable model performance, reporting mean and standard deviation of metrics across folds.
- Model comparison performed side-by-side, selecting the best model based on both **performance metrics** and **interpretability**.
- Additional analysis:
  - Random Forest **feature importance** visualization to understand influential features.
- The best performing model is ready for downstream tasks, including explainability and deployment.

---

## Author

Chekole Majilan  
Week 5–6 Fraud Detection Project
