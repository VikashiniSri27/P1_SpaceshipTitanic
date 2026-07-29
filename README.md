# P1: Spaceship Titanic

## 📌 Overview

This repository contains my solution for the **Spaceship Titanic** Kaggle competition, completed as part of an **ML Engineer Assignment**.

The project demonstrates an end-to-end machine learning workflow, including data preprocessing, feature engineering, model training using **CatBoost**, and generation of predictions for the competition test set.

---

## 📂 Repository Structure

```text
ML-Engineer-Assignment/
│
├── P1_SpaceshipTitanic.ipynb      # Complete ML pipeline
├── submission_catboost.csv        # Final prediction file
├── requirements.txt               # Python dependencies
└── README.md                      # Project documentation
```

---

## 🎯 Problem Statement

Predict whether passengers aboard the fictional **Spaceship Titanic** were transported to another dimension during a spacetime anomaly.

This is a binary classification problem where the target variable is:

* **Transported = True**
* **Transported = False**

---

## 📊 Dataset

Dataset: **Kaggle Spaceship Titanic**

Download the dataset from:

https://www.kaggle.com/competitions/spaceship-titanic/data

After downloading, place the following files in the project directory before running the notebook:

```text
train.csv
test.csv
sample_submission.csv
```

> **Note:** The dataset is not included in this repository because it is publicly available from Kaggle.

---

## 🛠️ Workflow

* Data loading
* Data cleaning
* Missing value handling
* Exploratory Data Analysis (EDA)
* Feature engineering
* Categorical feature encoding
* Model training using CatBoost
* Prediction generation
* Submission file creation

---

## 🤖 Model

* **Algorithm:** CatBoost Classifier
* **Task:** Binary Classification

CatBoost was selected because it performs well on tabular datasets and effectively handles categorical features with minimal preprocessing.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/ML-Engineer-Assignment.git
cd ML-Engineer-Assignment
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
P1_SpaceshipTitanic.ipynb
```

---

## 📦 Dependencies

* Python 3.x
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* catboost

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

## 📄 Output

The notebook generates:

```text
submission_catboost.csv
```

This file is formatted for submission to the Kaggle competition.

---

## 📈 Results

* Successfully trained a CatBoost classification model.
* Generated predictions for the test dataset.
* Produced a Kaggle-compatible submission file.

---

## 🔮 Future Improvements

* Hyperparameter tuning
* Cross-validation
* Advanced feature engineering
* Ensemble models
* Model explainability using SHAP

---

## 👤 Author

**VikashiniSri**

---

## 🙏 Acknowledgements

* Kaggle – Spaceship Titanic Competition
* CatBoost
* Scikit-learn
* Python Open Source Community
