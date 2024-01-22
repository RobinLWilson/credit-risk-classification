# credit-risk-classification report

## Overview of the Analysis
Purpose: To build a model that can accurately predict the likelihood a borrower will repay a loan.

Financial Information:
Data Provided:
- dollar amount of loan
- interest rate of loan
- borrower's income
- borrower's debt to income ratio
- number of credit accounts the borrower has open
- number of derogatory marks against the borrower
- borrower's total debt
- current status of loan (0: healthy or 1: high risk of default)

Variables Used for Prediction and Machine Learning Process:
For the first logistic regression (using LogisticRegression from scikit-learn), the model used raw, unscaled data which meant that 75,036 data points were from healthy loans and 2,500 data points were from high risk loans.  The goal was to determine the likelihood a borrower in the sample data would likely repay or default on a loan.

For the second logistic regression, the modeul scaled the data using the RandomOverSampler from imbalanced-learn  which resulted in an even split of data with 56,271 healthy loans and 56,271 high risk loans.  The adjusted data points were used in a new LogisticRegression model (named ros-model).  The goal was to determine the likelihood a borrower in the sample data would likely repay or default on a loan.

## Results

* Machine Learning Model 1:
    * Precision: 100% precise in predicting healthy loans and 85% precise in predicting unhealthy loans
    * Accuracy: 99% accuracy rate
    * Recall: 99% recall in healthy loans and 91% recall in unhealthy loans


* Machine Learning Model 2:
    * Precision: 99% precise in predicting healthy loans and 99% precise in predicting unhealthy loans
    * Accuracy: 99% accuracy rate
    * Recall: 99% recall in healthy loans and 99% recall in unhealthy loans

## Summary
If a lender is trying to predict whether borrowers in healthy loans will repay their balance, I recommend using the first LogisticRegression model as that was 99% accurate and 100% precise for health loans.

However, if a lender is trying to minimize their losses, I recommend using the second model with the OverSampled data as this would result in a fewer loans defaulting as the model was 99% accurate and 99% precise in identifying which loans would not be repaid.



