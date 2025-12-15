# Breast Cancer Classification (Machine Learning)

## 📌 Project Overview
This project focuses on **binary classification of breast cancer tumors** as *benign* or *malignant* using classical Machine Learning techniques.  
The objective is not only to achieve high accuracy, but also to **prioritize recall of malignant cases**, which is critical in medical applications.

This project was developed as part of a **Machine Learning portfolio**, with emphasis on clean code, correct evaluation, and interpretability.

---

## 🧠 Problem Definition
Breast cancer diagnosis is a high-stakes classification problem:

- False negatives (malignant predicted as benign) can have severe consequences
- Therefore, evaluation focuses on **recall**, **precision**, and **ROC AUC**, not only accuracy

---

## 📊 Dataset
- **Name:** Breast Cancer Wisconsin (Diagnostic)
- **Source:** UCI Machine Learning Repository / `sklearn.datasets`
- **Samples:** 569
- **Features:** 30 numeric features computed from digitized images of fine needle aspirates (FNAs)
- **Target labels:**
  - `0` → Benign
  - `1` → Malignant

---

## ⚙️ Data Preprocessing
The following preprocessing steps were applied:

- Conversion of all features to numeric values
- Handling missing values using the median
- Removal of zero-variance features
- Train-test split with stratification
- Feature scaling using `StandardScaler` (fit on training data only)

These steps ensure model stability and prevent data leakage.

---

## 🤖 Model Used

### Logistic Regression (Final Model)
Chosen for:
- Strong baseline performance
- Interpretability (important in healthcare contexts)
- Robustness and fast convergence

**Model configuration:**
- `max_iter = 1000`
- `class_weight = "balanced"`

---

## 📈 Model Evaluation
The model was evaluated on a held-out test set using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix


📌 **Key Insight:**  
Recall for malignant tumors is **95%**, meaning very few dangerous false negatives.

---

## 🔍 Interpretability
Logistic Regression allows direct inspection of feature coefficients, making it possible to understand which features contribute most to malignancy predictions.  
This is a key advantage in medical and regulated domains.
