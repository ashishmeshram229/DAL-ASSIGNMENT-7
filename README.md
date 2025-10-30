# 🌍 Multiclass Classification Analysis — Statlog (Landsat Satellite)

### 📘 A Machine Learning Assignment Project  
**Author:** Ashish Meshram  
Comprehensive evaluation of multiple supervised learning models on the **UCI Statlog (Landsat Satellite)** dataset — including detailed comparison using **F1-Score**, **ROC-AUC**, and **Precision-Recall (PRC-AP)** metrics.

---

## 📂 Project Overview

This project implements and evaluates multiple **multiclass classification algorithms** to predict land-cover types based on satellite spectral data.  
The analysis integrates model performance metrics across different evaluation curves (ROC, PRC) and thresholds to ensure robust model interpretability and selection.

---

## 🧠 Objectives

- Conduct **baseline and advanced model evaluations**  
- Use **One-vs-Rest (OvR)** for multi-class ROC and PRC curve generation  
- Compare models using **Accuracy**, **F1-Score**, **ROC-AUC**, and **PRC-AP**  
- Recommend the **most balanced and reliable model**  
- Demonstrate a **worst-case (AUC < 0.5)** model for conceptual understanding  

---

## 🧾 Dataset Description

**Source:** [UCI Machine Learning Repository — Statlog (Landsat Satellite)](https://archive.ics.uci.edu/dataset/146/statlog+landsat+satellite)

| Attribute | Description |
|------------|-------------|
| **Training file** | `sat.trn` |
| **Test file** | `sat.tst` |
| **Features** | 36 spectral bands per pixel |
| **Target variable** | Land cover class (1–7 → relabeled 1–6) |
| **Train size** | 4,435 samples |
| **Test size** | 2,000 samples |
| **Goal** | Predict correct land-cover type for each pixel |

---

## ⚙️ Project Workflow

### **1. Data Loading & Preparation**
```python
train_url = "data/sat.trn"
test_url  = "data/sat.tst"

column_names = [f'feature_{i}' for i in range(1, 37)] + ['class']
train_data = pd.read_csv(train_url, sep=' ', names=column_names, header=None)
test_data  = pd.read_csv(test_url,  sep=' ', names=column_names, header=None)

# Fix class labels (replace 7 → 6 for consistency)
train_data['class'] = train_data['class'].replace(7, 6)
test_data['class']  = test_data['class'].replace(7, 6)
