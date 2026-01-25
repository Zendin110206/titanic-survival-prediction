# Titanic: Machine Learning from Disaster

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn%20%7C%20Pandas%20%7C%20Seaborn-orange)
![Type](https://img.shields.io/badge/Type-Guided%20Learning%20Project-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview
This project is a classic **Binary Classification** problem in Data Science. The goal is to build a predictive model that answers the question: **"What sorts of people were more likely to survive?"** using passenger data (ie name, age, gender, socio-economic class, etc).

This project goes beyond simple tutorial following; it involves **critical questioning** of standard practices, deep-diving into Scikit-Learn pipelines, and validating hypotheses against historical logic.

## 🏆 Achievement
- **Best Model:** Random Forest Classifier (GridSearch Tuned)
- **Validation Score:** 82.86%
- **Kaggle Public Score:** **0.76555** (Top 76% accuracy for a first attempt!)

## 💾 Dataset
The dataset is sourced from the legendary Kaggle competition.
- **Source:** [Kaggle - Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)
- **Files:** `train.csv` (891 samples), `test.csv` (418 samples).
- **Key Features Engineered:** 
    - `Family_Size_Grouped` (Alone, Small, Medium, Large)
    - `Title` (Extracted from Name)
    - `TicketNumberCounts` (Grouping shared tickets)

## 📚 Learning Resource & Attribution
This project is a **code-along implementation** based on the comprehensive walkthrough by **Ryan & Matt Data Science**: 
[Beginner Data Science Portfolio Project Walkthrough (Kaggle Titanic)](https://www.youtube.com/watch?v=6IGx7ZZdS74&t=1208s).

> **Note:** I executed the code manually (no copy-paste) to ensure a deep understanding of every logical step, adding my own detailed comments, business interpretations, and critical validation.

## 🧠 My Critical Analysis & Key Learnings
During the development, I actively challenged and validated several concepts:

1.  **The "Data Leakage" Trap:**
    *   *Question:* Can we leave the `Survived` column in `X` if the Pipeline drops it later?
    *   *Finding:* Technically yes, but it's bad practice. Separating Feature (X) and Target (y) early is crucial to prevent accidental leakage.

2.  **The "Missing Fare" Anomaly:**
    *   *Problem:* The `test.csv` had 1 missing `Fare` value which broke the manual binning logic.
    *   *Solution:* Instead of relying on the pipeline's imputer (which runs later), I performed a strategic fill (using mean) *before* discretization to ensure the data wasn't lost during the binning process.

3.  **Pipeline vs Manual Processing:**
    *   *Insight:* I learned that `X_train` doesn't need to be manually cleaned before `.fit()`. The Pipeline acts as an automated factory that cleans, transforms, and trains the model in one go, ensuring `train` and `test` data are treated identically.

## 🛠️ Tech Stack
- **Data Manipulation:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn`
    - **Pipeline:** `make_pipeline`
    - **Preprocessing:** `ColumnTransformer`, `OneHotEncoder`, `OrdinalEncoder`, `SimpleImputer`
    - **Model:** `RandomForestClassifier`
    - **Tuning:** `GridSearchCV`, `StratifiedKFold`

## 📂 Project Structure

```
├── data/
│   └── train.csv # Training set
│   ├── test.csv # Test set
│   └── gender_submission.csv
├── notebooks/
│   └── titanic_classification.ipynb 
│       # Main Analysis Notebook
│
├── requirements.txt
│   # Python dependencies
│
└── README.md
    # Project documentation
```

---

_Implementation by [Muhammad Zaenal Abidin Abdurrahman](https://www.linkedin.com/in/zendin1102/) - 2026_
