# Initial Hospital Stay Prediction (Random Forest Regression)

## Overview
This project builds a Random Forest Regression model to predict the initial number of days a patient spends in the hospital using demographic, medical, and lifestyle features. The goal is to help healthcare organizations improve staffing, resource allocation, and patient care planning.

## Business Question
Can the Random Forest method be used to accurately predict the initial days a patient spends in the hospital using the available data?

## Dataset
- Medical records containing demographic, clinical, and lifestyle variables
- Target variable: Initial_days (number of days spent in the hospital)

Cleaned datasets and train/test splits are stored in the data/ folder.

## Data Preparation
- Removed duplicates and checked for missing values
- Identified and capped outliers using Z‑score thresholds
- Converted Yes/No variables to binary (1/0)
- Encoded multi‑category variables using LabelEncoder
- Dropped irrelevant ID columns
- Selected statistically significant predictors using SelectKBest (f_regression)

## Modeling Approach
- Algorithm: Random Forest Regressor
- Train/test split: 80/20
- Feature selection using SelectKBest
- Model trained with 200 estimators and a fixed random state
- Predictions evaluated using MSE, RMSE, and R²

## Results
- Mean Squared Error (MSE): 13.55
- Root Mean Squared Error (RMSE): 3.68
- R²: 0.98

## Insights
- The model explains 98% of the variance in initial hospital stay length Predictions deviate from actual values by approximately 3.7 days on average
- Selected features provide strong predictive power and highlight key factors influencing hospital stay duration
- The model performs well across a wide target range (1–71 days)
- Predictions can support staffing and resource distribution, helping ensure availability of staff, equipment, and hospital beds
- Anticipated stay lengths can improve admission and discharge planning, reducing bottlenecks
- Hospitals can develop personalized care plans for patients predicted to have longer stays

## Conclusion
The Random Forest model demonstrates excellent predictive performance and provides actionable insights for hospital operations. Predictions can support staffing decisions, resource planning, and targeted patient care strategies. With further tuning or additional features, the model could be enhanced even more.

The complete project report is available in the docs/ folder.


