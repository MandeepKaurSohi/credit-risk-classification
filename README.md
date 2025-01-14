
## Overview of the Analysis

Developing and assessing a machine learning model that forecasts loans' risk level as either healthy (low-risk) or non-healthy (high-risk) was the aim of this investigation. Financial institutions use this prediction to evaluate loan applications, lower risks, and make sure that decisions are well-informed.

Financial characteristics such loan amount, interest rate, borrower income, debt-to-income ratio, number of accounts, negative marks, and total debt are all included in the dataset. Loan_status, the target variable, categorises loans as either high-risk (1) or healthy (0). There was a class imbalance in the sample, with just 2,500 high-risk loans and 75,036 healthy loans.

## Stages of the Machine Learning Process

Data preprocessing: The dataset was divided into the target variable (y) and features (X). The model was trained using the features, and evaluation and prediction were done using the target variable.

Data Splitting: To guarantee reproducibility, the data was separated into training and testing sets using train_test_split with a random state of 1.

Model Selection: Because of its effectiveness and interpretability in binary classification problems, logistic regression was selected for this investigation.

Model Training and Prediction: The training dataset was used to train the logistic regression model, which was then applied to the testing dataset to generate predictions.

Model Evaluation: The model's performance was assessed using the classification report, confusion matrix, and balanced accuracy score.


## Results

Machine Learning Model 1: Logistic Regression
* Accuracy: The model achieved a high balanced accuracy score of 96.8%.
* Confusion Matrix:
* True Negatives: 18,655
* False Positives: 110
* False Negatives: 36
* True Positives: 583
* Classification Report:
* Healthy Loans (label 0):
> Precision: 1.00
> Recall: 0.99
> F1-Score: 1.00
> Support: 18,765
* High-Risk Loans (label 1):
> Precision: 0.84
> Recall: 0.94
> F1-Score: 0.89
> Support: 619
* Weighted Average Metrics:
> Precision: 0.99
> Recall: 0.99
> F1-Score: 0.99
> Support: 19,384
## Summary

The logistic regression model demonstrated remarkable performance, attaining a balanced accuracy of 96.8% and an overall accuracy of 99%. With a flawless precision of 1.00 and a recall of 0.99, its precision and recall ratings show that it is quite successful at recognising healthy loans (label 0). The model obtained a precision of 0.84 and a recall of 0.94 for high-risk loans (label 1), which is respectable but marginally less accurate because of the dataset's class imbalance.

## Recommedation
The logistic regression model is appropriate for forecasting loan statuses due to its strong overall performance. The program does a better job of detecting healthy loans than high-risk ones, though. If correctly forecasting high-risk loans is the company's top priority (label 1), additional steps like:

either undersampling the dominant class or oversampling the minority class (e.g., SMOTE).
using different algorithms that are better at handling unbalanced data, like as Random Forest or XGBoost.
The logistic regression model can be used exactly as is if the main goal is to balance correctly predicting both labels.

