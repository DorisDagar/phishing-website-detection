![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![LightGBM](https://img.shields.io/badge/LightGBM-Model-success)

# 🛡️ Phishing Website Detection using Machine Learning

An end-to-end Machine Learning project for phishing website detection using multiple supervised learning algorithms. The project covers the complete machine learning pipeline, including data preprocessing, exploratory data analysis, feature engineering, model development, hyperparameter tuning, model evaluation, model interpretability using SHAP, and deployment preparation.

---

## 📌 Project Overview

Phishing websites are designed to imitate legitimate websites and deceive users into revealing sensitive information such as usernames, passwords, and financial details. Detecting these malicious websites at an early stage is essential for improving cybersecurity and protecting users from online fraud.

This project aims to develop a robust machine learning model capable of accurately classifying websites as **Legitimate** or **Phishing**. Multiple machine learning algorithms were implemented and compared, with **LightGBM** selected as the final model based on its overall performance.

---

## 🎯 Project Objectives

- Understand and explore the phishing website dataset.
- Perform data preprocessing and feature engineering.
- Build and compare multiple machine learning models.
- Optimize the best-performing model using GridSearchCV.
- Evaluate model performance using multiple classification metrics.
- Interpret model predictions using Feature Importance and SHAP.
- Prepare the trained model for deployment.

---

## 📊 Dataset

**Dataset:** Phishing Websites Dataset

**Source:** UCI Machine Learning Repository

https://archive.ics.uci.edu/ml/datasets/phishing+websites

### Dataset Summary

- **Number of Samples:** 11,055
- **Number of Features:** 30
- **Target Classes:**
  - Legitimate Website
  - Phishing Website

---

## 🔄 Project Pipeline

```text
Dataset Understanding
        │
        ▼
Data Preprocessing
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Feature Engineering
        │
        ▼
Baseline Model Building
        │
        ▼
Hyperparameter Tuning
        │
        ▼
Model Evaluation
        │
        ▼
Model Interpretability (SHAP)
        │
        ▼
Deployment Preparation
```

---

## 📒 Notebook Guide

| Notebook | Description |
|-----------|-------------|
| **01** | Dataset Understanding |
| **02** | Data Preprocessing |
| **03** | Exploratory Data Analysis |
| **04** | Feature Engineering |
| **05** | Baseline Model Building |
| **06** | Hyperparameter Tuning (GridSearchCV) |
| **07** | Model Evaluation |
| **08** | Model Interpretability (Feature Importance & SHAP) |
| **09** | Deployment Preparation |

---

## 🤖 Machine Learning Models Implemented

The following machine learning models were implemented and compared:

- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost
- CatBoost
- LightGBM

---

## 🏆 Best Model

**LightGBM Classifier**

After comparing multiple machine learning models and performing hyperparameter tuning, **LightGBM** achieved the best overall performance and was selected as the final model for deployment.

### Final Performance

| Metric | Score |
|---------|------:|
| **Accuracy** | **83.54%** |
| **Precision** | **89.95%** |
| **Recall** | **87.60%** |
| **F1-Score** | **88.76%** |

The tuned **LightGBM** model achieved the highest overall performance among all evaluated models and was therefore selected as the final model for deployment.

---

## 📈 Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Classification Report

---

## 🔍 Model Interpretability

To improve model transparency and interpretability, the following Explainable AI (XAI) techniques were used:

- Feature Importance
- SHAP (SHapley Additive exPlanations) curve

These techniques provide insights into how individual features influence the model's predictions, making the model more transparent and trustworthy.

---

## 🚀 Deployment

The trained LightGBM model has been prepared for deployment by:

- Saving the trained model
- Loading the saved model
- Creating reusable prediction helper functions
- Testing the prediction pipeline
- Saving feature names required for inference

The project is deployment-ready and can be easily integrated into applications such as a Streamlit web application.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- LightGBM
- XGBoost
- CatBoost
- SHAP
- Joblib
- Jupyter Notebook

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/DorisDagar/phishing-website-detection.git
```

Navigate to the project directory:

```bash
cd phishing-website-detection
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

Run the notebooks in the following order:

1. Dataset Understanding
2. Data Preprocessing
3. Exploratory Data Analysis
4. Feature Engineering
5. Baseline Model Building
6. Hyperparameter Tuning
7. Model Evaluation
8. Model Interpretability
9. Deployment Preparation

---

## 📌 Future Improvements

- Develop a Streamlit web application for real-time phishing website detection.
- Evaluate the model using multiple phishing website datasets.
- Perform cross-dataset validation to improve generalization.
- Explore deep learning approaches for phishing website detection.
- Deploy the application on a cloud platform for public access.

---

## 📚 Literature Review

A comprehensive literature review was conducted by studying recent research papers on phishing website detection. The identified research gaps helped guide the design, implementation, and evaluation of this project.

---

## 👨‍💻 Author

**Doris Dagar**

B.Tech Computer Science & Engineering (Artificial Intelligence)

Indira Gandhi Delhi Technical University for Women (IGDTUW)

*This project was developed as part of a Machine Learning internship to demonstrate an end-to-end workflow for phishing website detection, covering data preprocessing, model development, model interpretability, and deployment preparation.*

---

## 🙏 Acknowledgements

- UCI Machine Learning Repository
- Scikit-learn
- LightGBM
- XGBoost
- CatBoost
- SHAP
- Open Source Machine Learning Community
