# Health Insurance Cost Prediction

## Project Overview
This project focuses on predicting health insurance costs using various regression models, including Linear Regression, Ridge Regression, and XGBoost. The objective is to analyze the factors influencing insurance costs and provide insights into potential overcharges or undercharges for different customer segments.

## Dataset
The dataset contains information about customers' age, number of dependents, income level, insurance plan type, and other relevant features. Through exploratory data analysis, we discovered that age is a significant predictor of insurance costs, with particular challenges in accurately predicting costs for the younger age group (below 25 years).

## Models Used
We implemented three models to predict health insurance costs:

1. **Linear Regression**
   - Train Score: 0.9282
   - Test Score: 0.9281
   - MSE: 5,165,611.91
   - RMSE: 2,272.80

2. **Ridge Regression**
   - Train Score: 0.9282
   - Test Score: 0.9281
   - MSE: 5,165,652.02
   - RMSE: 2,272.81

3. **XGBoost**
   - Train Score: 0.9809 (after hyperparameter tuning)
   - Test Score: 0.9782
   - MSE: 1,563,064.13
   - RMSE: 1,250.23

## Key Findings
- **Extreme Errors**: Approximately 30% of the predictions have an error margin of 10% or more, with a significant portion of these errors originating from the age group under 25.
- **High Overcharge/Undercharge Cases**: For ~3.6% of the customers (549 instances), the error exceeds 50%, leading to overcharges or undercharges of insurance costs.
- **Age-based Modeling**: Due to the prevalence of extreme errors in the under-25 age group, a separate model may be necessary for this segment.

## Features Analyzed
- Age
- Number of Dependents
- Income Level
- Insurance Plan
- BMI Category
- Smoking Status
- Employment Status
- Region

## Feature Importance
Feature importance analysis revealed that Age, Income, and Insurance Plan Type are among the top contributors to insurance cost variation.

## Error Analysis
- **Extreme Error Threshold**: Defined as predictions with a difference of 10% or more from the actual cost.
- **Distribution**: The residual analysis showed that most extreme errors occur for customers under 25 years of age.



