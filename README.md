--------------------------------------------------------------------------------
#Improving Diabetes Detection Using K-Fold Cross Validation and Feature Selection
This repository contains the complete implementation and documentation of a machine learning project focused on enhancing the detection of Diabetes Mellitus. The project addresses critical methodological gaps in existing research, specifically the "Recall Gap" caused by imbalanced datasets and the lack of robust feature selection.
The project follows a full research lifecycle, including proposal formulation, progress reporting, experimental validation, and final reporting in IEEE format.

--------------------------------------------------------------------------------
Project Overview
Early detection of diabetes is vital to prevent severe complications such as kidney failure and heart disease. However, real-world medical datasets like the Pima Indian Diabetes Dataset (PIDD) are inherently imbalanced, leading many models to achieve high overall accuracy while failing to identify true positive cases (low recall).
This project addresses these challenges by:
• Handling Class Imbalance: Using Synthetic Minority Over-sampling Technique (SMOTE) to balance the dataset.
• Optimal Feature Selection: Implementing Recursive Feature Elimination (RFE) to identify the most predictive clinical indicators.
• Robust Validation: Utilizing 5-Fold Cross Validation to ensure the model generalizes well to unseen data.
• Fair Evaluation: Shifting focus from simple accuracy to Precision, Recall, F1-Score, and ROC-AUC.

--------------------------------------------------------------------------------
Key Contributions
• Replication of Baseline Models: Validation of six standard models (LR, SVM, RF, KNN, DT, NB) showing they often miss over 50% of diabetic cases (Recall 0.39–0.49).
• Feature Optimization: Demonstration that RFE-selected features (like Glucose and BMI) can improve accuracy up to 78.2% compared to non-selected datasets.
• Imbalance Mitigation: SMOTE implementation to artificially balance the 500:268 ratio of non-diabetic to diabetic samples.
• Clinical Decision Support: Development of an integrated pipeline that prioritizes minimizing False Negatives for safer medical diagnosis.

--------------------------------------------------------------------------------
Reports
This repository includes formal academic reports documenting the project's evolution:
• Project Proposal: Defines research gaps, motivation, and the proposed integrated methodology.
• Progress Report: Documents data cleaning (median imputation), baseline results, and initial SMOTE testing.
• Final Report: Presents the complete performance analysis of the RFE-SMOTE-Pipeline in IEEE style.

--------------------------------------------------------------------------------
Dataset
• Name: Pima Indians Diabetes Database (PIDD)
• Source: UCI Machine Learning Repository
• Size: 768 samples (female patients, ≥ 21 years old)
• Features: 8 clinical attributes (Pregnancies, Glucose, BP, Skin Thickness, Insulin, BMI, Pedigree, Age)
• Class Distribution:
    ◦ Non-diabetic (0): 65.1% (500 samples)
    ◦ Diabetic (1): 34.9% (268 samples)

--------------------------------------------------------------------------------
Methodology Summary
Baseline Models
• Logistic Regression (LR)
• Support Vector Machine (SVM)
• Decision Tree (DT) & Random Forest (RF)
• K-Nearest Neighbors (KNN)
• Naive Bayes (NB)
Advanced Approaches (Proposed)
• SMOTE-enhanced Pipeline: Synthetic data generation for the minority class.
• RFE Wrapper Method: Iterative feature removal based on model weights.
• 5-Fold Cross Validation: Ensuring performance consistency across five different data folds.
Evaluation Metrics
• Recall (Sensitivity): Primary metric for minimizing missed diagnoses.
• ROC-AUC: Assessing the discriminative ability of the model.
• Precision & F1-Score.

--------------------------------------------------------------------------------
Experimental Environment
• Language: Python 3.12
• Libraries: scikit-learn, imbalanced-learn, pandas, Matplotlib
• Platform: Google Colab / Jupyter Notebook

--------------------------------------------------------------------------------
Results Summary
• Baseline models achieve high accuracy (~77-97%) but suffer from a "Recall Gap" (0.39–0.49).
• Integration of SMOTE is expected to boost Recall for the diabetic class by ≈ 20-30%.
• RFE simplifies the model by focusing on 5 key features (Glucose, BMI, Age, Insulin, Pregnancies).
• 5-Fold CV provides a more objective performance estimate compared to a 70:30 random split.

--------------------------------------------------------------------------------
Authors
Syaukas Rahmatillah
Department of Informatics
Syiah Kuala University, Banda Aceh, Indonesia
Email: syakas@mhs.usk.ac.id

Muhammad Ali Murtaza
Department of Informatics
Syiah Kuala University, Banda Aceh, Indonesia
Email: alibungker@gmail.com

--------------------------------------------------------------------------------
License
This project is intended for academic and educational purposes only. Please cite appropriately if you reuse any part of this work.

--------------------------------------------------------------------------------
Analogi: Repositori ini bukan sekadar melatih model untuk menebak siapa yang sakit (Akurasi), melainkan melatih model untuk tidak pernah melewatkan orang yang benar-benar membutuhkan bantuan medis (Recall) dengan bantuan "latihan sintetis" (SMOTE) dan fokus pada "gejala inti" (RFE).
