# Titanic---Machine-Learning-from-Disaster-
Use the model trained based on passenger data (ie name, age, gender, socio-economic class, etc) to predict whether or not people in test set survived the sinking of the Titanic.

## Project Overview
This project applies several machine learning models to the Titanic dataset to predict passenger survival.
The goal is to practice a complete supervised learning workflow, including data preprocessing, feature engineering, model training, parameter tuning, and model comparison.

## Dataset
The dataset comes from the Kaggle Titanic competition and contains passenger information such as age, sex, ticket class, fare, and family relationships.

- Training set: includes survival labels
- Test set: used for final prediction submission

## Data Preprocessing
Several preprocessing steps were applied:

- Filled missing values in numerical features (Age, Fare) using median values
- Filled missing values in categorical features (Embarked) using the most frequent category
- Encoded categorical variables such as Sex and Embarked into numerical form
- Dropped the Cabin feature due to excessive missing values

## Feature Engineering
To capture additional information, several new features were created:

- FamilySize: number of family members traveling together
- IsAlone: whether a passenger traveled alone
- Title: extracted from passenger names and grouped into major categories

These engineered features help the model better represent social and family-related survival patterns.

## Model Training Validation
The dataset was split into training and validation sets(80/20 split).
Multiple models were trained and evaluated on the validation set:

- Logistic Regression
- Random Forest
- Gradient Boosting
- XGBoost

Hyperparameter tuning was performed using GridSearchCV with 5-hold cross-validation.
Model performance was compared using validation accuracy.

## Results
Among the tested models, Gradient Boosting achieved the highest validation accuracy.
Based on this result, the tuned Gradient Boosting model was selected for final prediction on the test set.

## Final Output
The final model was used to generate survival predictions for the test dataset, and the results were saved as a CSV file suitable for Kaggle submission. 

## What I Learned
Through this project, I gained hands-on experience with:

- End-to-end machine learning workflows
- Feature engineering and its impact on model performance
- Model comparison and hyperparameter tuning
- Practical use of cross-validation for model selection
