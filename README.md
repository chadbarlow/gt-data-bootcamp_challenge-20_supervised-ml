<h1 align="left">SUPERVISED MACHINE LEARNING<br><i>Credit Risk Classification Report</i> </h1> 

## Overview

- **Objective**  
The purpose of this analysis was to build machine learning models to predict whether a loan is high risk or healthy based on financial data. The aim was to assist financial institutions in making more informed decisions when approving loans, minimizing the risk of defaults. 

The dataset contained detailed financial information including loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The target variable was a binary label indicating whether a loan was high risk ('1') or healthy ('0').

- **Method**  
The original data was highly imbalanced, with a significantly larger number of healthy loans compared to high-risk loans. We discovered the imbalance with `value_counts`. To address the issue, we performed data resampling using the `RandomOverSampler` method from the `imbalanced-learn` library. Two machine learning models were built as part of this analysis: one with the original, imbalanced data and another with the oversampled data. Both models used logistic regression.

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

Both models performed well, with high accuracy, precision, recall, and F1-scores for both classes. However, the second model, which used oversampling to balance the classes, performed slightly better in terms of identifying high-risk loans (recall for high-risk loans was 0.99 compared to 0.91 in the first model). The choice of model depends on the priority of the financial institution. If the priority is to minimize false negatives (i.e., high-risk loans incorrectly classified as healthy), then the second model is preferable due to its higher recall for high-risk loans. However, this comes at the cost of slightly lower precision, meaning it might classify a few more healthy loans as high-risk. If it's more important to minimize false positives (i.e., healthy loans incorrectly classified as high-risk), then the first model, which has higher precision for high-risk loans, might be preferable. However, this comes at the cost of missing some high-risk loans. **However, given the high costs associated with approving high-risk loans, the second model (with oversampling) might be a better choice as it is more conservative and better at catching high-risk loans.**

## Limitations and Further Development
- Perform feature engineering (e.g. PCA Analysis) to identify the most important features for credit risk prediction.
- Perform alternative resamplings. Oversampling improved the performance of our model on the minority class. Other resampling techniques, such as under-sampling the majority class or using a combination of over- and under-sampling, might further improve performance while also hedging against the risk of overfitting.
