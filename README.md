Biological ML Classifier: Predicting Malignant vs Benign Cell States
This project builds a machine‑learning classifier to distinguish malignant from benign breast cell samples using quantitative morphological features.
The dataset used is the Breast Cancer Wisconsin Diagnostic (WDBC) dataset, which contains measurements extracted from digitised images of cell nuclei.
The goal is to demonstrate:
biological interpretability
reproducible ML workflow
clear evaluation metrics
clean, admissions‑ready project structure
1. Project Motivation
Accurate early detection of malignancy is essential in cancer diagnostics.
Cell nuclei from malignant tumours typically show:
increased size
irregular boundaries
distorted membrane structure
loss of smoothness
Machine learning can quantify these patterns and classify malignancy with high accuracy.
This project demonstrates how ML can extract biologically meaningful signals from morphological data.
2. Dataset Overview
Dataset: Breast Cancer Wisconsin Diagnostic (WDBC)
Samples: 569
Features: 30 continuous morphological measurements
Label:
M → malignant
B → benign
Features include:
radius
perimeter
area
concavity
compactness
smoothness
fractal dimension
All features are derived from cell‑nucleus morphology.
3. Repository Structure
data/
raw/ → original wdbc.data file
processed/ → cleaned dataset used for modelling
notebooks/
01_preprocessing_and_exploration.ipynb
02_model_training_and_evaluation.ipynb
03_feature_importance_and_biology.ipynb
04_clean_results_only.ipynb
figures/
ROC curves
confusion matrices
feature importance plot
4. Methods
Preprocessing
Load raw dataset
Assign official WDBC column names
Encode labels (M → 1, B → 0)
Drop ID column
Scale features using StandardScaler
Save processed dataset
Models Trained
Logistic Regression
Random Forest
Evaluation Metrics
Accuracy
ROC‑AUC
ROC curves
Confusion matrices
Interpretability
Random Forest feature importance
Biological interpretation of top predictors
5. Results
Model Performance
Random Forest achieved the strongest performance with high accuracy and AUC.
ROC Curves
[Looks like the result wasn't safe to show. Let's switch things up and try something else!]
Confusion Matrices
Logistic Regression
[Looks like the result wasn't safe to show. Let's switch things up and try something else!]
Random Forest
[Looks like the result wasn't safe to show. Let's switch things up and try something else!]
Feature Importance
[Looks like the result wasn't safe to show. Let's switch things up and try something else!]
6. Biological Interpretation
The model identifies morphological irregularity as the strongest predictor of malignancy.
Key biological insights:
radius_worst, perimeter_worst, area_worst  
Larger, more irregular nuclei — a hallmark of malignant transformation.
concave_points_worst, concavity_mean  
Distorted membrane structure and nuclear indentation, common in invasive cancer cells.
compactness_mean, smoothness_worst  
Loss of structural integrity and increased boundary irregularity.
These findings align with known histopathological features of malignant breast tissue.
7. Conclusion
This project demonstrates how machine learning can classify malignancy from quantitative cell‑nucleus features with high accuracy and clear biological interpretability.
It provides:
a reproducible ML workflow
biologically grounded interpretation
clean, admissions‑ready documentation
This project forms one of the core components of a computational biology portfolio alongside RNA‑seq analysis and flow‑cytometry QC.
