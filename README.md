# Titanic Survival Prediction with Classical Machine Learning
Use the model trained based on passenger data (ie name, age, gender, socio-economic class, etc) to predict whether or not people in test set survived the sinking of the Titanic.

## Project Motivation
The Titanic dataset is a canonical benchmark for supervised learning, but its true value lies in illustrating the complete reasoning process behind feature engineering and model evaluation.

This project focuses on understanding how structured passenger data can be transformed into meaningful features and how different modeling choices influence predictive performance.

## Dataset & Task Definition 
The dataset used in this project is a publicly available Titanic passenger dataset, containing demographic and ticket-related information of passengers.

- **Task type:** Binary classification (Survived / Not Survived)
- **Input:** Tabular features such as age, sex, fare, family relations, and ticket class
- **Output:** Survival probability

The dataset presents common real-world challenges, including missing values and mixed data types.

## Methodology
The workflow emphasizes correctness and interpretability rather than model complexity:

1. Data cleaning and missing value handling  
2. Feature extraction from raw text fields (e.g., titles from names)  
3. Encoding categorical variables  
4. Train–validation split to prevent data leakage  
5. Baseline model training and comparison  

## Feature Engineering
To capture additional information, several new features were created:

- FamilySize: number of family members traveling together
- IsAlone: whether a passenger traveled alone
- Title: extracted from passenger names and grouped into major categories

These engineered features help the model better represent social and family-related survival patterns.

## Model & Evaluation
Several classical models were explored, including logistic regression and tree-based methods:
- Logistic Regression
- Random Forest
- Gradient Boosting
- XGBoost

Evaluation focused on:
- Accuracy for baseline comparison
- Cross-validation consistency
- Interpretability of learned patterns

## Results
Different classical models were compared under a consistent validation setting. Gradient Boosting showed the strongest validation performance among the tested approaches, indicating that ensemble methods were effective at capturing non-linear patterns in the data.

## Key Takeaways
This project strengthened foundational skills in:
- Feature engineering for tabular data
- Preventing data leakage
- Interpreting model performance beyond raw accuracy
