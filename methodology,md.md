Methodology

Diabetes Prediction Using Machine Learning

1. Research Question

Can machine learning models accurately predict diabetes using patient health-related features? This project aims to compare Logistic Regression and Random Forest models for diabetes classification.

2. Dataset Description

Dataset Name: Pima Indians Diabetes Dataset

Source: Kaggle

Dataset Size: 768 records and 9 columns.

The dataset contains health-related information used to predict whether a patient has diabetes.

Features:

1. Pregnancies
2. Glucose
3. BloodPressure
4. SkinThickness
5. Insulin
6. BMI
7. DiabetesPedigreeFunction
8. Age

Target Variable:

- Outcome = 0: Non-diabetic
- Outcome = 1: Diabetic

3. Dataset Limitations

- The dataset contains only 768 records.
- The target classes are imbalanced, with 500 non-diabetic and 268 diabetic records.
- Several medical measurements contain invalid zero values.
- The dataset represents a specific population and may not generalize to all populations.
- The dataset has a limited number of features.

4. Data Cleaning Plan

The following data cleaning steps will be performed:

- Check missing values in all columns.
- Identify invalid zero values in Glucose, BloodPressure, SkinThickness, Insulin, and BMI.
- Replace invalid zero values with missing values (NaN).
- Remove duplicate records.
- Use median imputation to handle missing values.

Median imputation will be fitted using training data to avoid data leakage.

5. Feature Engineering

A new interaction feature will be created using Glucose and BMI.

New Feature:

Glucose_BMI = Glucose × BMI

This feature represents the interaction between two health-related measurements and will be investigated for its potential contribution to diabetes prediction.

6. Machine Learning Models

Two classification algorithms will be used:

1. Logistic Regression

Logistic Regression will be used as a baseline classification model. It is suitable for binary classification and provides an interpretable approach to predicting diabetes.

2. Random Forest Classifier

Random Forest combines multiple decision trees to improve classification performance. It can capture nonlinear relationships between features and is suitable for comparing against Logistic Regression.

7. Data Preprocessing

The following preprocessing techniques will be applied:

- Median Imputation: To handle missing values.
- Standard Scaling: To normalize feature scales.
- Pipeline: To organize preprocessing and model training and reduce data leakage.

8. Train-Test Split

The dataset will be divided into:

- 80% Training Data
- 20% Testing Data

Stratified sampling will be used to maintain the proportion of both target classes in the training and testing sets.

Random state will be set to 42 for reproducibility.

9. Evaluation Metrics

The models will be evaluated using the following metrics:

Accuracy: Measures the overall proportion of correct predictions.

Precision: Measures how many predicted diabetic cases are actually diabetic.

Recall: Measures how many actual diabetic cases are correctly identified.

F1-score: Provides a balance between Precision and Recall.

ROC-AUC: Measures the model's ability to distinguish between diabetic and non-diabetic classes across different classification thresholds.

These metrics will help compare the performance of Logistic Regression and Random Forest.

10. Experimental Workflow

The project will follow these steps:

1. Load the Pima Indians Diabetes Dataset.
2. Explore dataset information and distributions.
3. Identify and handle invalid zero values.
4. Remove duplicate records.
5. Create the Glucose_BMI interaction feature.
6. Separate input features and target variable.
7. Split the data into training and testing sets.
8. Apply median imputation and feature scaling.
9. Train Logistic Regression and Random Forest models.
10. Evaluate and compare model performance using the selected metrics.

11. Expected Outcome

The experiment aims to identify which of the two machine learning models performs better on the selected dataset. The results will be compar