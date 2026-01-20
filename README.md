# Titanic: Machine Learning from Disaster

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn%20%7C%20Pandas%20%7C%20Seaborn-orange)
![Type](https://img.shields.io/badge/Type-Guided%20Learning%20Project-green)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

## 📌 Project Overview
This project is a classic **Binary Classification** problem in Data Science. The goal is to build a predictive model that answers the question: **"What sorts of people were more likely to survive?"** using passenger data (ie name, age, gender, socio-economic class, etc).

This serves as my foundational project to master **Supervised Learning** and **Data Preprocessing pipelines**.

## 💾 Dataset
The dataset is sourced from the legendary Kaggle competition.
- **Source:** [Kaggle - Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)
- **Description:** 
    - `train.csv`: Data used to train the model (contains the target label `Survived`).
    - `test.csv`: Data used to validate the model's performance.
- **Key Features:** `Pclass` (Ticket Class), `Sex`, `Age`, `SibSp` (Siblings/Spouse), `Parch` (Parents/Children), `Fare`.

> **Note:** The dataset files are included in the `data/` folder for reproducibility.

## 📚 Learning Resource & Attribution
This project is a **code-along implementation** based on the comprehensive walkthrough by **Ryan & Matt Data Science**: 
[Beginner Data Science Portfolio Project Walkthrough (Kaggle Titanic)](https://www.youtube.com/watch?v=i_LwzRVP7bg).

> **Note:** I executed the code manually (no copy-paste) to ensure a deep understanding of every logical step, adding my own detailed comments, logic breakdown, and exploration notes.

## 🎯 Learning Objectives
By working on this project, I aim to master the following concepts (Continuously Updated):
1.  **Exploratory Data Analysis (EDA):** Understanding correlations between survival rates and demographic features (e.g., "Women and Children First").
2.  **Advanced Data Cleaning:** Handling missing values (Imputation) for `Age` and `Cabin` columns strategically.
3.  **Feature Engineering:** 
    - Transforming categorical data (Text) into numerical format (Encoding).
    - Creating new features to improve model accuracy.
4.  **Model Building:** Implementing Classification algorithms (Logistic Regression, Random Forest, etc.) using `scikit-learn`.
5.  **Evaluation:** Measuring accuracy and submitting predictions to Kaggle.

## 🛠️ Tech Stack
- **Data Manipulation:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn` (Pipeline, Imputer, Encoder, Classifier)
- **Environment:** Jupyter Notebook

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
