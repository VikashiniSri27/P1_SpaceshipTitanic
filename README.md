# P1: Spaceship Titanic

## 📌 Overview
This repository contains my solution for the **Spaceship Titanic** Kaggle competition, completed as part of an **ML Engineer Assignment**.

The project demonstrates an end-to-end machine learning workflow, including data preprocessing, feature engineering, model training using **CatBoost**, cross-validation, threshold tuning, and generation of predictions for the competition test set.

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
* Feature engineering (Cabin split into Deck/CabinNum/Side, TotalSpending, NoSpending flag)
* Categorical feature encoding
* Baseline model training (RandomForest)
* Final model training using CatBoost
* 5-fold stratified cross-validation
* Decision threshold tuning
* Prediction generation
* Submission file creation

---

## 🤖 Model
* **Algorithm:** CatBoost Classifier
* **Task:** Binary Classification

CatBoost was selected because it performs well on tabular datasets and effectively handles categorical features with minimal preprocessing.

**Hyperparameters:**
* `iterations`: 500
* `learning_rate`: 0.05
* `depth`: 6
* `random_seed`: 42

---

## 🚀 Getting Started

This project was built and run in **Google Colab**.

### 1. Open the notebook in Colab
Upload `P1_SpaceshipTitanic.ipynb` to Google Drive, then open it with Colab (or use **File → Upload notebook** directly from the Colab interface).

### 2. Upload the dataset
Upload `train.csv`, `test.csv`, and `sample_submission.csv` to the Colab session's working directory using the file upload icon in the left sidebar (or mount Google Drive and point to the file locations).

### 3. Install dependencies
The first cell installs any packages not already available in the Colab runtime:
```python
!pip install catboost
```
All other dependencies (`pandas`, `numpy`, `matplotlib`, `scikit-learn`) come pre-installed in Colab.

### 4. Run all cells
**Runtime → Run all**

This runs the full pipeline end-to-end and produces `submission_catboost.csv` in the Colab working directory, which you can download from the file sidebar.

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

| Metric | Value |
|---|---|
| CV Accuracy (mean) | 0.8155 |
| CV Accuracy (std) | 0.0059 |
| Validation Accuracy (threshold 0.5) | 0.8097 |
| Validation Accuracy (tuned threshold 0.60) | 0.8235 |
| Precision | 0.8045 |
| Recall | 0.8219 |
| F1 Score | 0.8131 |
| ROC-AUC | 0.9168 |
| Log Loss | 0.3556 |
| Kaggle Public Score | 0.80804 |

* Trained a CatBoost classifier with 5-fold stratified cross-validation.
* Tuned the decision threshold (default 0.5 → 0.60), improving validation accuracy by ~1.4 points.
* Generated predictions for the test dataset using the tuned threshold.
* Produced a Kaggle-compatible submission file.

---

## 🔮 Future Improvements
* Hyperparameter tuning (grid/random/Bayesian search)
* Cross-validated threshold selection (to reduce sensitivity to a single validation split)
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
