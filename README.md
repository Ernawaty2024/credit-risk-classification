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

### 3. Write a Credit Risk Analysis Report
A brief report summarizing the model's performance was written. This report, included in the README.md file, covers the following key points:

## Credit Risk Analysis Report

### Overview of the Analysis
The purpose of this analysis was to build a logistic regression model to predict the credit risk (healthy or high-risk) of loans using historical lending data. The model was designed to assist the lending services company in identifying the creditworthiness of potential borrowers.

### Results
The logistic regression model's performance was evaluated with the following key metrics:
- **Accuracy Score**: `99%`
- **Precision Score**:
**Precision (Healthy Loan - 0)**: `100%` 
**Precision (High-Risk Loan - 1)**: `85%` 
- **Recall Score**: 
**Recall (Healthy Loan - 0)**: `99%`
**Recall (High-Risk Loan - 1)**: `94%`

The specific performance metrics were as follows:
- True Negatives (Healthy loans predicted correctly): `55,967`
- False Positives (Healthy loans predicted as high-risk): `310`
- False Negatives (High-risk loans predicted as healthy): `116`
- True Positives (High-risk loans predicted correctly): `1,759`

### Classification Report:

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| **0** | 1.00      | 0.99   | 1.00     | 56,277  |
| **1** | 0.85      | 0.94   | 0.89     | 1,875   |

- **Macro Average Precision**: 0.92
- **Macro Average Recall**: 0.97
- **Weighted Average Precision**: 0.99
- **Weighted Average Recall**: 0.99

## Summary

The machine learning model achieves a high accuracy of 99%, demonstrating strong performance in predicting both healthy and high-risk loans. The precision for healthy loans is perfect (100%), meaning that the model almost never incorrectly classifies a healthy loan as high-risk. However, the precision for high-risk loans is 85%, indicating that 15% of loans predicted to be high-risk are actually healthy.

The recall for high-risk loans is 94%, which means the model correctly identifies 94% of high-risk loans. This high recall for high-risk loans suggests that the model is reliable in detecting risky borrowers, which is crucial for financial institutions looking to minimize defaults.

### Recommendation:
Given the high accuracy, strong precision, and recall for both classes, this model is recommended for identifying the creditworthiness of borrowers. However, additional tuning could be done to further improve the precision for high-risk loans to minimize false positives, thereby ensuring fewer healthy loans are misclassified as high-risk.


