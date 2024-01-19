# credit-risk-classification

## Overview of the Analysis

In this project, various techniques to train and evaluate a model based on loan risk. Using a dataset of historical lending activity from a peer-to-peer lending services company we built a model that can identify the creditworthiness of borrowers.

The data has multiple features :

- the size of the loan (loan_size)
- its interest rate (interest_rate)
- the borrower's income (borrower_income)
- the debt to income ratio (debt_to_income)
- the number of accounts the borrower holds (num_of_accounts)
- derogatory marks against the borrower (derogatory_marks)
- the total debt (total_debt)

We need to predict loan_status(A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting)

Following steps were performed to create a Logistic Regression Model with the Original Data and Resampled Data:

    1. Fit a logistic regression model by using the training data (X_train and y_train).

    2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

    3. Evaluate the model’s performance by doing the following:

    4. Generate a confusion matrix.

    5. Print the classification report.

## Results

**Machine Learning Model 1:**
_Precision_: 94% (average)
For predicting low-risk loans, the model was 100% precise, however the model was only 87% precise in predicting high-risk loans
_Accuracy_: 94%
_Recall_: 94% (average)
For predicting low-risk loans the model had 100% recall, but 89% recall in predicting high-risk loans

**Machine Learning Model 2:**
_Precision_: 94% (average)
For predicting low-risk loans, the model was 100% precise, however the model was only 87% precise in predicting high-risk loans
_Accuracy_: 99.59%
_Recall_: 100% (average)
For predicting both low and high-risk loans the model had 100% recall

## Summary

Machine Learning Model 2 is less likely to predict false negative results (2 vs 67). However, based on the confusion matrices for each model, Machine Learning Model 2 predicted slightly more (91 vs 80) false positives (low-risk when the actual was high-risk).

If the goal of the model is to determine the likelihood of high-risk loans, neither model scores above 95% precision. Machine Learning Model 2 had fewer false predictions of the testing data overall and would be the best model to use based on the high accuracy and recall of this model.
