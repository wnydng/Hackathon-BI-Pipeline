# Fraud Detection using Machine Learning (LightGBM)

## Overview
This project applies Machine Learning methods to detect fraudulent transactions. The goal is to predict whether a transaction is fraudulent (1) or non-fraudulent (0) based on financial and behavioral data. The model was developed as part of a Machine Learning project at ESILV.

## Objectives
- Build a supervised model to detect fraud in financial transactions.
- Handle class imbalance and ensure realistic evaluation using temporal validation.
- Generate a CSV file for submission containing: transaction_id, fraud_prediction.
- Compare multiple algorithms and select the most effective one.

## Dataset
The dataset contains information about customers and their transactions. Some key features include transaction_id, card_id, amount, credit_limit, mcc, credit_score, total_debt, yearly_income, age_group, and fraud (target variable). After cleaning and feature engineering, around 30 relevant features were used to train the model.

## Methodology
Data Preparation: Cleaned and encoded categorical columns such as mcc and age_group. Scaled numerical variables using a standard scaler. Used a temporal split to separate training and testing data, ensuring time-based validation.

Model Selection: The following models were tested — LightGBM, XGBoost, CatBoost, Logistic Regression, Balanced Random Forest, EasyEnsemble, and TabNet. Among them, LightGBM showed the best balance between performance and computation time.

Model Training: The final model was trained using Light Gradient Boosting Machine (LightGBM) with temporal split (80% training, 20% testing). Key parameters included n_estimators = 800, learning_rate = 0.03, num_leaves = 64, and scale_pos_weight adjusted for class imbalance.

## Results
| Metric | Value |
|--------|--------|
| Recall | 0.79 |
| Specificity | 0.75 |
| F1-score | 0.009 |
| AUC | 0.80 |

The LightGBM model achieved good performance, successfully detecting most fraudulent transactions while keeping false positives under control.

## Output
The model creates a file called fraud_predictions_final.csv containing transaction_id and fraud_prediction columns. Example summary:
Total transactions evaluated: 50,000  
Predicted fraudulent (1): 380 (0.76%)  
Predicted non-fraudulent (0): 49,620 (99.24%)  
This reflects realistic fraud occurrence levels in financial data.



## Interpretation
This project uses the LightGBM algorithm to identify fraudulent transactions using machine learning. The model learns from customer and transaction patterns to predict fraud risk effectively. The generated CSV file can be used for reporting, further evaluation, or real-time fraud monitoring.



