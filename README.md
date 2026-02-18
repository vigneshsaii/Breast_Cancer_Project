
# Breast Cancer Prediction System

## Overview

This project builds a supervised machine learning model to classify breast tumors as malignant or benign using diagnostic measurement data. The objective is to assist early detection by providing a reliable predictive system based on numerical tumor features.

The system leverages statistical learning techniques to support medical decision-making through accurate classification.

---

## Problem Statement

Breast cancer is one of the most common cancers worldwide. Early detection significantly increases survival rates. Manual diagnosis based purely on visual interpretation can be subjective and time-consuming.

This project develops a machine learning classifier that predicts whether a tumor is malignant or benign using diagnostic measurements.

---

## Dataset Description

The model is trained on the Wisconsin Breast Cancer dataset.

Dataset characteristics:

* 569 instances
* 30 numerical features
* No missing values
* Binary target variable

Target variable:

* 0 → Malignant
* 1 → Benign

Features include:

* Radius
* Texture
* Perimeter
* Area
* Smoothness
* Concavity
* Symmetry
* Fractal dimension

These measurements are computed from digitized images of fine needle aspirate (FNA) of breast masses.

---

## System Architecture

Data Loading → Data Cleaning → Feature Scaling → Model Training → Model Evaluation → Prediction

The pipeline is designed to avoid data leakage by fitting scaling parameters only on training data.

---

## Data Preprocessing

* Removed irrelevant columns (ID fields)
* Checked for missing values
* Standardized numerical features using StandardScaler
* Performed train-test split (80-20)

Scaling was essential because Logistic Regression is sensitive to feature magnitude.

---

## Model Implementation

The primary model implemented:

* Logistic Regression

Why Logistic Regression?

* Interpretable coefficients
* Efficient for binary classification
* Works well with linearly separable datasets
* Strong baseline with low computational cost

---

## Model Performance

Training Accuracy: 97.3%
Test Accuracy: 92.98%

Evaluation Metrics Used:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

High test accuracy indicates strong generalization capability.

---

## Key Observations

* Tumor size-related features (radius, perimeter, area) significantly influence predictions.
* Concavity and texture measurements strongly differentiate malignant from benign cases.
* Model performance suggests features are well-separated in feature space.

---

## Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## Scalability & Improvements

To make this system more production-ready:

* Add cross-validation for robustness
* Implement hyperparameter tuning
* Add ROC-AUC analysis
* Introduce alternative models (Random Forest, SVM, XGBoost)
* Add SHAP for explainability
* Deploy as REST API

---

## Limitations

* Dataset size is relatively small
* Real-world medical diagnosis requires more complex validation
* Model should not be used as a sole diagnostic tool

This system is intended as a predictive support tool, not a replacement for clinical evaluation.

---

## Conclusion

This project demonstrates strong fundamentals in supervised machine learning, feature scaling, evaluation metrics, and model validation. It reflects the ability to build structured ML pipelines and evaluate model performance using statistical reasoning.
