Machine Learning Assignment - Diabetes Readmission Classification

Problem Statement
Hospital readmissions among diabetic patients increase healthcare costs and place additional burden on hospitals. The objective of this project is to develop and compare multiple machine learning classification models to predict patient readmission status using demographic, clinical, laboratory, and medication-related attributes from diabetic patient records.

Dataset - Diabetes 130-US Hospitals for Years 1999–2008
Dataset Description:
Dataset Name: Diabetes 130-US Hospitals for Years 1999–2008
Source: Kaggle Machine Learning Repository
Number of Instances: 101,766
Number of Features: 50
Target Variable: readmitted
Classes:NO,30, <30
Dataset Characteristics:

- Mixed categorical and numerical features
- Missing values present
- Multi-class classification problem
- Imbalanced class distribution


Project Status
✅ Phase 1 Completed – Problem Framing & Data Audit

✅ Phase 2 Completed – Data Preprocessing

✅ Phase 3 Completed – Machine Learning Model Training & Evaluation

Completed Tasks
Phase 1 - Data Audit
Dataset loading
Dataset audit
Missing value analysis
Duplicate analysis
Feature type identification
Class distribution analysis
Class imbalance analysis
Phase 2 - Data Preprocessing
Identifier column removal
Missing value handling
Categorical encoding
Feature scaling
Train-test split (80:20)
Stratified sampling
Leakage prevention using Pipeline and ColumnTransformer
Phase 3 - Model Training & Evaluation
Logistic Regression
Decision Tree Classifier
K-Nearest Neighbors (KNN)
Gaussian Naive Bayes
Random Forest Classifier
Accuracy Evaluation
AUC Evaluation
Precision Evaluation
Recall Evaluation
F1 Score Evaluation
MCC Evaluation
Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-Learn
Joblib

Data Preprocessing: 
The following preprocessing steps were performed:

Missing value handling
Duplicate inspection
Removal of identifier columns:
encounter_id
patient_nbr
One-Hot Encoding of categorical features
Standard Scaling of numerical features
Stratified Train-Test Split (80:20)
Leakage prevention using Pipeline and ColumnTransformer


Model Comparison Results:
ML Model	Accuracy	AUC	Precision	Recall	F1 Score	MCC
Logistic Regression	0.5743	0.6476	0.4723	0.4002	0.3808	0.1804
Decision Tree	0.5005	0.5501	0.3948	0.3925	0.3931	0.1162
KNN	0.5067	0.5836	0.4044	0.3987	0.4000	0.1236
Naive Bayes	0.1365	0.5058	0.3727	0.3404	0.1094	0.0178
Random Forest	0.5847	0.6570	0.5348	0.4045	0.3804	0.1999

Model Observations: 
- Logistic Regression: Achieved strong overall performance with good Accuracy and AUC. Provided stable predictions across all classes.

-Decision Tree: Captured non-linear relationships but achieved lower Accuracy and MCC compared to ensemble techniques.

-KNN: Achieved the highest F1 Score, indicating balanced classification performance, although overall Accuracy was lower than Random Forest.

-Naive Bayes: Produced the weakest performance. The independence assumption did not fit the highly correlated healthcare features.

- Random Forest:Achieved the best overall performance with the highest Accuracy, AUC, Precision, and MCC scores.

Model Performance Visualization:
A graphical comparison of all evaluation metrics (Accuracy, AUC, Precision, Recall, F1 Score, and MCC) has been generated and saved as - outputs/model_comparison_graph.png

Overall Winner: Random Forest

Performance Highlights:

Accuracy: 0.5847
AUC: 0.6570
Precision: 0.5348
MCC: 0.1999
Random Forest was selected as the final recommended model because it achieved the strongest overall performance across the evaluation metrics.

GitHub Repository
Repository Link:

https://github.com/2026CT05197/ML-Classification-Assignment

Repository Structure
ML_Diabetes_Readmission_Project
│
├── README.md
├── requirements.txt
├── diabetic_data.csv
├── IDS_mapping.csv
├── test_data.csv
│
├── model/
│   └── .gitkeep
│
├── outputs/
│   ├── model_comparison_graph.png
│   └── model_comparison_results.csv
│
└── diabetes_classification.ipynb