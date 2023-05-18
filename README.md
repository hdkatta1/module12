# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of this analysis is to build and evaluate machine learning models for credit risk classification. The dataset used in this analysis is historical lending activity from a peer-to-peer lending services company. The dataset is imbalanced, with healthy loans outnumbering high-risk loans.
* Explain what financial information the data was on, and what you needed to predict.

The dataset used in this analysis contains historical lending activity data from a peer-to-peer lending services company. The dataset includes various financial information related to borrowers, such as their income, debt-to-income ratio, loan amount, interest rate, and employment length, among others.

The goal of the analysis is to predict the creditworthiness of borrowers based on the provided financial information. Specifically, the task is to predict whether a loan is classified as "healthy" or "high-risk." In the dataset, a value of 0 in the "loan_status" column indicates a healthy loan, while a value of 1 indicates a high-risk loan.

By training machine learning models on this data, we aim to develop models that can accurately classify loans as either healthy or high-risk based on the borrowers' financial information. This helps lenders in assessing the risk associated with potential borrowers and making informed decisions regarding loan approvals.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
In this analysis, the target variable we were trying to predict is the "loan_status," which indicates whether a loan is considered healthy (0) or high-risk (1). The dataset was heavily imbalanced, with 75,036 instances of healthy loans (0) and 2,500 instances of high-risk loans (1) in the original dataset.
* Describe the stages of the machine learning process you went through as part of this analysis.
Data Split: The dataset was divided into training and testing sets.with 75% of the data used for training and 25% for testing.

Model Development - First Model: Logistic regression model was trained using the training set. 

Evaluation of the First Model: Performance metrics such as accuracy, confusion matrix, and classification report were calculated for the first model.These metrics provided insights into the model's ability to predict both healthy and high-risk loans.

Model Development - Second Model: Random oversampling was applied to the training data, followed by training a logistic regression model, ensuring an equal number of instances for both healthy and high-risk loans

Evaluation of the Second Model: Performance metrics were calculated for the second model trained on the resampled data.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
The logistic regression algorithm was used in both models to predict the loan status based on the provided features such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt.
In the second model, we used a method called random oversampling. This helps to increase the number of high-risk loans in the training data. This helps the logistic regression model to learn more about high-risk loans and make better predictions for them. By balancing the number of healthy and high-risk loans, the model becomes more accurate in identifying and classifying high-risk loans.
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  Logistic Regression Model with Original Data
Balanced Accuracy Score: 0.994
Precision Score (healthy loans): 1.000
Precision Score (high-risk loans): 0.839
Recall Score (healthy loans): 0.994
Recall Score (high-risk loans): 0.992



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  Logistic Regression Model with Resampled Training Data
Balanced Accuracy Score: 0.994
Precision Score (healthy loans): 1.000
Precision Score (high-risk loans): 0.839
Recall Score (healthy loans): 0.994
Recall Score (high-risk loans): 0.992

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
Both the logistic regression models with original and resampled training data performed well in predicting the creditworthiness of borrowers. The models had high accuracy scores of 0.994 and high precision scores for healthy loans. However, the precision score for high-risk loans was low at 0.839, indicating that there were still a number of false positives.

Based on the performance metrics, there was no significant improvement in using the resampled data for training the logistic regression model. Therefore, we recommend using the original dataset with the logistic regression model for credit risk classification. However, it is important to note that the precision score for high-risk loans could still be improved.


