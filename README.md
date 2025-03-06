## HR Leads Prediction

This project aims to predict high-potential HR service leads based on funding and hiring trends using machine learning.

## Project Overview
In this challenge, we analyze company data, including industry, hiring trends, and funding information, to determine whether a company is a potential lead (`is_hot_lead`). A **Random Forest Classifier** is used for predictions.

## Dataset
- **Source:** Provided by the competition.
- **Features:**  
  - *industry* - Industry type  
  - *hiring_roles* - Number of hiring roles  
  - *last_funding_date* - Date of the last funding  
  - *funding_amount* - Amount of funding received  
  - Other relevant company attributes.
- **Target Variable:** *is_hot_lead* (1 - Hot Lead, 0 - Not a Hot Lead)

## Preprocessing Steps
- Converted last_funding_date to datetime format.
- Encoded categorical features (industry, hiring_roles) using Label Encoding.
- Handled missing values by replacing `NaN` with the median.
- Removed infinite values by replacing them with NaN.

## Model & Training
- **Algorithm Used:** `RandomForestClassifier`
- **Hyperparameters:** 100 estimators, random state = 42
- **Training Data:** 80% of the dataset
- **Test Data:** 20% of the dataset

## Evaluation
- The model is evaluated using the **F1-Score**.
- **Example output:**
  
  F1-Score: 0.85
