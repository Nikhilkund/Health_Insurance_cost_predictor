Health Insurance Cost Prediction
This project focuses on predicting health insurance costs using various regression models, including Linear Regression, Ridge Regression, and XGBoost. The objective is to analyze the factors influencing insurance costs and provide insights into potential overcharges or undercharges for different customer segments.

Project Overview
The dataset used contains information about customers' age, number of dependents, income level, insurance plan type, and other relevant features. Through exploratory data analysis, we discovered that age is a significant predictor of insurance costs, with a particular challenge in accurately predicting costs for the younger age group (below 25 years).

We implemented three models:

Linear Regression
Ridge Regression
XGBoost
XGBoost outperformed other models with a high R-squared value and lower Root Mean Squared Error (RMSE).

Key Findings
Extreme Errors: Approximately 30% of the predictions have an error margin of 10% or more, with a significant portion of these errors originating from the age group under 25.
High Overcharge/Undercharge Cases: For ~3.6% of the customers (549 instances), the error exceeds 50%, leading to overcharges or undercharges of insurance costs.
Age-based Modeling: Due to the prevalence of extreme errors in the under-25 age group, I concluded that a separate model might be necessary for this segment. I am currently building a Streamlit app to handle predictions for customers aged 25 and older, as there is insufficient data for reliable predictions for younger customers.
Models
1. Linear Regression
Train Score: 0.9282
Test Score: 0.9281
MSE: 5,165,611.91
RMSE: 2,272.80
2. Ridge Regression
Train Score: 0.9282
Test Score: 0.9281
MSE: 5,165,652.02
RMSE: 2,272.81
3. XGBoost
Train Score: 0.9809 (after hyperparameter tuning)
Test Score: 0.9782
MSE: 1,563,064.13
RMSE: 1,250.23
Features
Age
Number of Dependents
Income Level
Insurance Plan
BMI Category
Smoking Status
Employment Status
Region
Feature Importance
Feature importance analysis revealed that Age, Income, and Insurance Plan Type are among the top contributors to insurance cost variation.

Error Analysis
Extreme Error Threshold: We defined extreme errors as predictions with a difference of 10% or more from the actual cost.
Distribution: The residual analysis showed that most extreme errors occur for customers under 25 years of age. Thus, a separate predictive model may be required for this age group.
Next Steps
Develop a separate model for customers under 25.
Improve data collection for the younger age group.
Continue building a Streamlit app to visualize the predictions for customers aged 25 and above.
Conclusion
This project highlights the challenges in predicting health insurance costs for younger customers and provides a robust model for the older age group. By analyzing extreme errors and identifying patterns, we can adjust pricing strategies to minimize overcharges or undercharges.
