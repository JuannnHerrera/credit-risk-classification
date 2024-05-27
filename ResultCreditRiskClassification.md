# Credit Risk Classification

## Overview of the Analysis

Alright, here's the lowdown. We set out to predict whether borrowers are going to pay back their loans or default, using some fancy machine learning techniques. We've got a dataset from a peer-to-peer lending service, and it includes all sorts of financial details like loan size, interest rate, borrower's income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. Our main goal is to figure out the `loan_status` - a value of 0 means the loan is healthy, while a value of 1 means it's high-risk.

### Financial Information in the Data
- **Loan Size:** How much the loan is for.
- **Interest Rate:** The interest rate applied to the loan.
- **Borrower Income:** The income of the person taking out the loan.
- **Debt-to-Income Ratio:** How much debt the borrower has compared to their income.
- **Number of Accounts:** How many financial accounts the borrower has.
- **Derogatory Marks:** Negative marks on the borrower's credit report.
- **Total Debt:** Total amount of debt the borrower has.

### Purpose of the Analysis
We want to build a machine learning model to predict if a loan will be paid back (healthy) or if it's going to be a problem (high-risk), based on the financial info we have.

### Stages of the Machine Learning Process
1. **Data Loading and Preprocessing:** First, we read the CSV file and get the data ready by splitting it into features (`X`) and labels (`y`).
2. **Data Splitting:** Then, we divide the data into training and testing sets.
3. **Model Training:** We train a logistic regression model using the training data.
4. **Model Prediction:** We make predictions on the testing data.
5. **Model Evaluation:** Finally, we evaluate how well our model did using a confusion matrix and classification report.

### Methods Used
- **Logistic Regression:** We used logistic regression to create our predictive model.

## Results

### Logistic Regression Model
- **Accuracy Score:** 0.99
- **Precision Score:**
  - For class 0 (healthy loan): 1.00
  - For class 1 (high-risk loan): 0.86
- **Recall Score:**
  - For class 0 (healthy loan): 1.00
  - For class 1 (high-risk loan): 0.91

## Summary

The logistic regression model is pretty solid, with an overall accuracy of 0.99. It's great at predicting healthy loans (class 0) with both precision and recall scores of 1.00. It's a bit less perfect with high-risk loans (class 1), scoring 0.86 in precision and 0.91 in recall.

### Recommendation
Given these results, the logistic regression model is reliable for predicting credit risk, especially for spotting healthy loans. This model can definitely be recommended for use by the company. It's super accurate in identifying healthy loans but slightly less so for high-risk loans. However, the high recall for high-risk loans (0.91) means it's good at catching most of the risky ones, which is crucial to avoid defaults.

If your main concern is accurately predicting high-risk loans to avoid defaults, this model does a good job but might need some tweaks or perhaps trying other algorithms to get even better precision for high-risk predictions.
