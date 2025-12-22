# Improving Diabetes Detection Using K-Fold Cross Validation and Feature Selection

This repository contains the complete implementation and documentation of a machine learning research project focused on improving **Diabetes Mellitus detection** by addressing two major methodological issues commonly found in prior studies: **class imbalance** and **suboptimal feature selection**.

The project follows a **full academic research lifecycle**, including proposal formulation, progress reporting, experimental evaluation, and final reporting using the **IEEE paper format**.

---

## 📌 Project Overview

Early detection of diabetes is crucial to prevent severe complications such as kidney failure, cardiovascular disease, and neuropathy. However, real-world medical datasets—such as the **Pima Indians Diabetes Dataset (PIDD)**—are inherently **imbalanced**, causing many machine learning models to achieve high accuracy while failing to correctly identify diabetic patients (low recall).

This project focuses on **minimizing false negatives** by shifting evaluation emphasis from accuracy to recall-oriented metrics and by introducing a robust integrated pipeline.

---

## 🔍 Key Contributions

- **Baseline Model Replication**  
  Six standard machine learning models (LR, SVM, RF, KNN, DT, NB) were replicated and evaluated, revealing that many models miss over **50% of diabetic cases** (Recall ≈ 0.39–0.49).

- **Feature Optimization using RFE**  
  Recursive Feature Elimination (RFE) identifies the most predictive clinical attributes, improving accuracy up to **78.2%**.

- **Class Imbalance Mitigation with SMOTE**  
  Synthetic Minority Over-sampling Technique (SMOTE) balances the original **500:268** class ratio.

- **Clinical Decision Support Perspective**  
  The proposed pipeline prioritizes **Recall** to minimize missed diagnoses.

---

## 📊 Dataset Information

- **Name**: Pima Indians Diabetes Dataset (PIDD)  
- **Source**: UCI Machine Learning Repository  
- **Samples**: 768 female patients (≥ 21 years old)  
- **Features**: 8 clinical attributes  
- **Target Variable**: Binary (0 = Non-diabetic, 1 = Diabetic)

---

## ⚙️ Methodology Summary

### Baseline Models
- Logistic Regression (LR)
- Support Vector Machine (SVM)
- Decision Tree (DT)
- Random Forest (RF)
- K-Nearest Neighbors (KNN)
- Naive Bayes (NB)

### Proposed Pipeline
- SMOTE-enhanced data balancing
- Recursive Feature Elimination (RFE)
- 5-Fold Cross Validation

---

## 📈 Evaluation Metrics

- Recall (Sensitivity)
- Precision
- F1-Score
- ROC-AUC

---

## 🧪 Experimental Environment

- Python 3.12
- scikit-learn
- imbalanced-learn
- pandas
- matplotlib
- Google Colab / Jupyter Notebook

---

## 👨‍💻 Authors

**Syaukas Rahmatillah**  
Department of Informatics  
Syiah Kuala University  
Email: syakas@mhs.usk.ac.id  

**Muhammad Ali Murtaza**  
Department of Informatics  
Syiah Kuala University  
Email: alibungker@gmail.com  

---

## 📜 License

This project is intended for academic and educational purposes only.
