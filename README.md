# Lung Cancer Survival Prediction 🩺🎯

This project aims to predict lung cancer **survival outcomes** using machine learning techniques on a large synthetic healthcare dataset. The project includes preprocessing, feature engineering, model training, evaluation, and deployment via a REST API.

---

## 📂 Project Structure
lung-cancer-prediction/
├── data/ # Raw and cleaned data files
├── notebooks/ # Jupyter notebooks for EDA and modeling
├── models/ # Saved ML models (.pkl)
├── app.py # Flask API app for deployment
├── test_api.py # Sample client script to test the API
├── requirements.txt # Python dependencies
├── README.md # Project overview
└── lung_cancer_pipeline.ipynb # Main training and evaluation pipelin

## 🧠 Problem Statement

Given a dataset of lung cancer patients containing clinical, demographic, and lifestyle attributes, **predict whether a patient will survive or not**.

**Target Variable**: `survived` (1 = Yes, 0 = No)

---

## 📊 Dataset Overview

The dataset includes the following key features:

- `age`, `gender`, `country`
- `cancer_stage`, `family_history`, `smoking_status`, `bmi`, `cholesterol_level`
- `hypertension`, `asthma`, `cirrhosis`, `other_cancer`
- `treatment_type`, `treatment_duration_days`
- Engineered features: `comorbidity_score`, `age_group`, `smoke_comorb`, etc.

Total samples: `890,000+`  
Balanced with downsampling and synthetic techniques.

---

## ⚙️ Models Trained

| Model               | Accuracy | F1-score (Class 1) | PR AUC |
|--------------------|----------|---------------------|--------|
| Logistic Regression | 0.49     | 0.31                | 0.22   |
| Decision Tree       | 0.32     | 0.35                | 0.22   |
| Random Forest       | 0.64     | 0.24                | 0.22   |
| XGBoost             | 0.78     | 0.00                | 0.22   |
| **Balanced RF ✅**     | *Tuned & Best* | *Improved F1*     | *✔️*     |

📌 *BalancedRandomForestClassifier from imblearn gave the best performance after tuning.*

---
