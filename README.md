# Credit Risk Classification Challenge

## Background 
In this challenge, various machine learning techniques are applied to train and evaluate a model based on loan risk. Using a dataset of historical lending activity from a peer-to-peer lending services company, the objective is to build a model capable of identifying the creditworthiness of borrowers.


## Instructions

### 1. Split the Data into Training and Testing Sets
The dataset `lending_data.csv` was read into a Pandas DataFrame. The `loan_status` column served as the labels set (`y`), where:
- `0` means the loan is healthy.
- `1` means the loan has a high risk of defaulting.

The features DataFrame (`X`) was created from the remaining columns.

The dataset was then split into training and testing sets using the `train_test_split` method from the `sklearn` library.

### 2. Create a Logistic Regression Model with the Original Data
A logistic regression model was trained with the original data:
- The training feature data (`X_train`) and the training labels (`y_train`) were used to fit the logistic regression model.
- The testing feature data (`X_test`) was used to generate predictions for the testing labels.

The model's performance was evaluated by:
- Generating a **confusion matrix** to summarize the prediction results.
- Printing the **classification report** to display precision, recall, and F1-score for each class.

The following question was answered: *How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?*

### 3. Write a Credit Risk Analysis Report
A brief report summarizing the model's performance was written. This report, included in the README.md file, covers the following key points:

## Credit Risk Analysis Report

### Overview of the Analysis
The purpose of this analysis was to build a logistic regression model to predict the credit risk (healthy or high-risk) of loans using historical lending data. The model was designed to assist the lending services company in identifying the creditworthiness of potential borrowers.

### Results
The logistic regression model's performance was evaluated with the following key metrics:
- **Accuracy Score**: The proportion of true results (both true positives and true negatives) among the total number of cases.
- **Precision Score**: The number of true positive predictions divided by the total number of positive predictions.
- **Recall Score**: The number of true positive predictions divided by the total number of actual positives (true positives and false negatives).

The specific performance metrics were as follows:
- **Accuracy**: `X%`
- **Precision (Healthy Loan - 0)**: `X%`
- **Precision (High-Risk Loan - 1)**: `X%`
- **Recall (Healthy Loan - 0)**: `X%`
- **Recall (High-Risk Loan - 1)**: `X%`

### Summary
The logistic regression model provided a reasonable prediction for both healthy and high-risk loans. Based on the accuracy, precision, and recall scores, the model is capable of correctly identifying the majority of high-risk loans. However, further fine-tuning may be required to improve the precision and recall for predicting high-risk loans, as false positives (predicting a loan as high-risk when it is healthy) could lead to missed lending opportunities.

Given the results, the model could be recommended as an initial screening tool for identifying credit risk. However, more sophisticated techniques, or an ensemble of models, might provide better performance for more accurate decision-making in loan issuance.
