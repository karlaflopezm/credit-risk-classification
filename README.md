# Credit Risk Classification

## Overview

In this project, the goal is to analyze historical lending activity from a peer-to-peer lending services company to build a model capable of identifying the creditworthiness of borrowers. By using machine learning techniques, the goal is to predict whether a loan is likely to be healthy (0) or high risk of default (1). A logistic regression model is used to classify loans based on features from the dataset.

The dataset provided consists of various attributes that might influence the risk of a loan default. The purpose of this analysis is to build and evaluate a predictive model that can help financial institutions make data-driven decisions on loan approvals.

## Instructions

1. **Split the Data into Training and Testing Sets**:  
   - Load the dataset and split it into features (X) and target labels (y), where the target variable is the `loan_status`.
   - Split the data into training and testing sets using `train_test_split`.

2. **Create a Logistic Regression Model**:  
   - Train a logistic regression model on the training data (`X_train`, `y_train`).
   - Predict the labels of the testing data (`X_test`) and evaluate the model's performance.

3. **Write a Credit Risk Analysis Report**:  
   - Generate a confusion matrix and print the classification report to evaluate how well the model performs.
   - Summarize the analysis and provide an assessment of the model’s ability to predict healthy loans (0) and high-risk loans (1).

## Results

- **Accuracy Score**:  
  The accuracy score of the logistic regression model on the testing data is approximately **99.4%**.

- **Precision Score**:  
  The precision score for predicting high-risk loans (1) is **84.08**.

- **Recall Score**:  
  The recall score for predicting high-risk loans (1) is **98.4**.

## Summary

The logistic regression model provides a reasonable prediction of both healthy loans and high-risk loans. The results indicate that the model is effective at identifying high-risk loans, but there may be areas of improvement in terms of precision or recall. Given these results, the model could be useful for assisting lenders in making more informed decisions about creditworthiness. However, further tuning and testing with other models may improve performance and robustness.

Based on the current analysis, I **recommend** using this logistic regression model as a starting point, but further steps should be taken to improve performance, especially in identifying high-risk loans with greater accuracy.

## Repository Structure

- `credit_risk_classification.ipynb`: Jupyter notebook containing the code for model training, testing, and evaluation.
- `lending_data.csv`: Dataset containing historical lending data.
- `README.md`: This file, containing an overview and analysis of the project.



