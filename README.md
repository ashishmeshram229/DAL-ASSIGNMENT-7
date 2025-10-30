# 🌍 DA5401 A7 — Model Selection (Landsat Satellite Classification)

**Author:** Ashish Meshram  
**Dataset:** [UCI Statlog (Landsat Satellite)](https://archive.ics.uci.edu/dataset/146/statlog+landsat+satellite)

---

## 🚀 Project Overview
A comparative analysis of multiple machine learning classifiers on the **Landsat Satellite** dataset.  
The goal is to evaluate and select the most reliable model based on **F1-Score**, **ROC-AUC**, and **PRC-AP** metrics.

---

## ⚙️ Models Evaluated
- **K-Nearest Neighbors (KNN)**
- **Support Vector Machine (SVM)**
- **Logistic Regression**
- **Decision Tree**
- **Naive Bayes (Gaussian)**
- **RandomForest**
- **XGBoost**
- **Dummy Classifier (Baseline)**
- **Inverted Model (AUC < 0.5 demo)**

---

## 📊 Key Results

| Model | Accuracy | F1-weighted | ROC-AUC | PRC-AP |
|--------|-----------|--------------|----------|---------|
| **KNN** | 0.904 | 0.9037 | 0.979 | 0.9217 |
| **SVM** | 0.895 | 0.8925 | 0.985 | 0.9177 |
| **RandomForest** | 0.911 | 0.9089 | 0.990 | 0.9518 |
| **XGBoost** | 0.905 | 0.9030 | 0.990 | 0.9509 |
| **Dummy Classifier** | 0.230 | 0.086 | 0.500 | 0.167 |

---

## 🧠 Insights
- **KNN** delivers the best balance across **precision, recall, and discrimination**.
- **SVM** shows superior ROC-AUC but slightly lower PRC performance.
- **Ensembles (RF, XGB)** achieve top overall metrics (>0.99 ROC-AUC).
- The **inverted RandomForest** effectively demonstrates an AUC < 0.5 “worse-than-random” case.

---

## 🏁 Final Recommendation
> **Best Overall Model:** 🥇 **K-Nearest Neighbors (k=5)**  
> Balanced, robust, and interpretable across all metrics.

---

## 🧩 Bonus (Brownie Points)
✅ Added **RandomForest** & **XGBoost** for ensemble benchmarking  
✅ Created **AUC < 0.5** demo via inverted/shuffled predictions  

---

📘 *By* **Ashish Meshram**  
*M.Tech in Data Science | GATE DA 2025 Aspirant*  
⭐ *If you found this project insightful, consider giving it a star!*
