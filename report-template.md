# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
    the goal was to analyze a dataset containing the financial details of historical loan recipients to develop a machine learning model capable of predicting the credit/loan risks for future applicants. Specifically, the objective was to create a model that could classify loan applicants as either high-risk (1) or low-risk (0). This classification would enable lenders—such as banks or private equity firms—to make more informed decisions and minimize the risk of loan defaults.

* Explain what financial information the data was on, and what you needed to predict.
    The provided dataset included several important financial indicators, such as loan size, interest rate, debt-to-income ratio, and derogatory marks, all of which are commonly used to assess a borrower’s financial health. Based on these features, the target variable was set to loan_status, which indicated whether a loan was high-risk or low-risk. The data was imbalanced, with 18,765 loans classified as low-risk (0) and only 619 loans labeled as high-risk (1).

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
    The target variable (loan status) has two possible outcomes:

        1 (High-risk): Represents applicants who are likely to default.

        0 (Low-risk): Represents applicants who are considered financially healthy.

* Describe the stages of the machine learning process you went through as part of this analysis.
    Data Preprocessing: The data was cleaned by handling missing values and encoding categorical variables. Features were selected based on relevance to loan default prediction.

    Feature Selection: I chose financial and demographic variables as features, excluding the target variable (loan_status).

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

        Model Selection and Training: Several machine learning models were applied, with a focus on models suitable for binary classification.

            Logistic Regression: A probabilistic model that estimates the likelihood of a loan being high-risk.

            Decision Tree: A tree-based model that splits data into segments based on certain thresholds

            Random Forest: An ensemble model that combines multiple decision trees to increase prediction accuracy and reduce overfitting.

    Model Evaluation: Models were evaluated using accuracy, precision, and recall scores to determine how well they predicted both the high-risk and low-risk applicants.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
        Model: Logistic Regression Results
        
            Accuracy: 99.36%

            Precision: 84.07%

            Recall: 98.39%

            Confusion Matrix:
            [[18652, 113],
            [10, 609]]
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
    The Logistic Regression model performs exceptionally well in predicting loan defaults, with a high overall accuracy of 99.37%. The recall score of 98.38% is especially strong, making the model highly effective at identifying high-risk applicants. This is crucial in financial decision-making, where minimizing defaults is of utmost importance. While the precision score is slightly lower (84.35%), this is manageable, as it means a small proportion of loans predicted as high-risk were actually low-risk. The model balances both precision and recall well.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
    Given the high recall and solid precision, Logistic Regression is recommended for this analysis. The model performs reliably in identifying high-risk loans, which is the priority in predicting defaults.

    If a different problem required a focus on minimizing false positives (predicting low-risk loans), then we could explore other models or adjustments to the threshold. However, for this task — identifying loan defaults — the Logistic Regression model stands out as the most appropriate choice.

    
