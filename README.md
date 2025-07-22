# 🚀 PolyBagML: A Custom Approach for High-Dimensional Intrusion Dataset Prediction

**PolyBagML** is a high-performance machine learning framework designed to handle real-world network intrusion detection problems. Built using **ensemble decision trees** and **XGBoost**, it is optimized for **high-dimensional**, **noisy**, and **imbalanced** datasets like Distributed Denial of Service (DDOS).

---

## 📌 Overview

PolyBagML is a custom ensemble algorithm that:
- Trains multiple decision trees on various bootstrapped subsets
- Uses polynomial feature extraction to capture complex nonlinear relationships
- Supports XGBoost for gradient-boosted learning
- Handles missing values, categorical features, and high cardinality

---

## 🧠 Model Features

- ✅ Custom ensemble logic (bagging + boosting)
- ✅ Polynomial feature expansion (degree = 2)
- ✅ Missing value imputation (median strategy)
- ✅ Categorical hashing for label encoding
- ✅ Evaluation via MSE, R², RMSE, confusion matrix, and classification accuracy

---

## 🗂️ Dataset

- **File**: `DDoSdata(1).csv`
- **Rows**: 20,000+ (assumed)
- **Columns**: Network flow features (source IP, dest IP, flags, duration, etc.)
- **Target**: Binary classification (Attack = 1, Normal = 0)

---

## 📈 Performance Results

### ✅ Regression Metrics (PolyBagML):

| Model              | MSE              | R² Score          |
|------------------- |------------------|-------------------|
| PolyBagML (DT)     | 1.12e-07         | 0.999996          |
| PolyBagML (XGBoost)| 2.87e-11         | 1.000000 ✅      |

## 📉 RMSE vs Epoch Graph

- Steep decline in early rounds → fast learning  
- Flattens near zero by round 25 → optimal convergence

---

## 🧪 Evaluation Metrics Summary

- 🔵 **R² Score**: Measures how close predictions are to actual values (ideal: 1.0)
- 🔵 **MSE / RMSE**: Penalizes large prediction errors
- 🔵 **Accuracy** (via Confusion Matrix): 100% for both normal and attack traffic

---

## 💡 Future Scope

🔮 **Deploy as a Web App:**
- Host PolyBagML on a frontend with file upload functionality
- Users can drag and drop **raw/unprocessed datasets**
- The system will:
  1. Detect unsuitable or missing formats
  2. Automatically clean, encode, and transform the dataset
  3. Run inference and return results + accuracy report

🔮 **Enhance with Larger/Complex Datasets:**
- Test PolyBagML with advanced datasets
- Expand to multi-class classification (not just binary)

🔮 **AutoML Capabilities:**
- Integrate feature selection, hyperparameter tuning, and real-time model evaluation
- Support exporting models to ONNX or TensorFlow Lite for deployment on edge devices

---

## 🧰 Tech Stack

- Python 3.9+
- Libraries: `pandas`, `numpy`, `scikit-learn`, `xgboost`, `matplotlib`
- Jupyter Notebook /
- Dataset: `.csv` format, requires preprocessing

---
Copyright © 2025 Raakesh Kripal VUK

This code and its content may not be used, copied, modified, published, or distributed without the author's prior written consent.

Contact: raakeshkripal.vuk@gmail.com
