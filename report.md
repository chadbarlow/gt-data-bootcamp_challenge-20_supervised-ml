# Project Report 

## Overview of the Analysis

- **Explain the purpose of the analysis.**  
The purpose of this analysis was to build machine learning models to predict whether a loan is high risk or healthy based on financial data. The aim was to assist financial institutions in making more informed decisions when approving loans, minimizing the risk of defaults.

- **Explain what financial information the data was on, and what you needed to predict.**  
The dataset contained detailed financial information including loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The target variable was a binary label indicating whether a loan was high risk ('1') or healthy ('0').

- **Provide basic information about the variables you were trying to predict (e.g., `value_counts`).**  
The original data was highly imbalanced, with a significantly larger number of healthy loans compared to high-risk loans. We discovered the imbalance with `value_counts`. To address the issue, we performed data resampling using the `RandomOverSampler` method from the `imbalanced-learn` library.

- **Describe the stages of the machine learning process you went through as part of this analysis.**  
Two machine learning models were built as part of this analysis: one with the original, imbalanced data and another with the oversampled data. Both models used logistic regression.

## Results

- **Machine Learning Model 1 (without oversampling):**
    - **Overall Performance**
        - Accuracy: 0.99
    - **Healthy Loans** 
        - Precision: 1.00
        - Recall: 0.99
        - F1-score: 1.00
    - **High-Risk Loans**
        - Precision: 0.85
        - Recall: 0.91
        - F1-score: 0.88

- **Machine Learning Model 2 (with oversampling):**
    - **Overall Performance**
        - Accuracy: 0.99
    - **Healthy Loans** 
        - Precision: 1.00
        - Recall: 0.99
        - F1-score: 1.00
    - **High-Risk Loans**
        - Precision: 0.84
        - Recall: 0.99
        - F1-score: 0.91

## Summary

Both models performed well, with high accuracy, precision, recall, and F1-scores for both classes. However, the second model, which used oversampling to balance the classes, performed slightly better in terms of identifying high-risk loans (recall for high-risk loans was 0.99 compared to 0.91 in the first model).

The choice of model depends on the priority of the financial institution. If the priority is to minimize false negatives (i.e., high-risk loans incorrectly classified as healthy), then the second model is preferable due to its higher recall for high-risk loans. However, this comes at the cost of slightly lower precision, meaning it might classify a few more healthy loans as high-risk.

If it's more important to minimize false positives (i.e., healthy loans incorrectly classified as high-risk), then the first model, which has higher precision for high-risk loans, might be preferable. However, this comes at the cost of missing some high-risk loans.

**In my opinion, given the high costs associated with approving high-risk loans, the second model (with oversampling) might be a better choice as it is more conservative and better at catching high-risk loans.**
