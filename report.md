# Module 12 Report

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of this analysis is to train and predict to see if our model, (specifically the Logistic Regression model), accurately predicts the potential observations for healthy and risky loans.

* Explain what financial information the data was on, and what you needed to predict.
The financial information was based on historical lending activity data composed of features such as: loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, total_debt. Along with our features, we would try to solve for loan status or what the positive observation would be (high_risk loans) as it deviates from what the prediction not of interest would be (healthy loans). The total amount of possible outcomes is 77,536 with associated features.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The 0 label dictates healthy loans and the 1 dictates high-risk loans.

* Describe the stages of the machine learning process you went through as part of this analysis.
The stages of the machine learning process follows this sequence:
  - Initialize the DataFrame and seperate the feature variables from the target variables
  - initialize your testing and training variables by using the train_test_split function
  - initialize your Logistic Regression model and fit by using the training variables you seperated
  - With the Logisitc Regression modeled now trained, input the classifier model with your Test variables to output your predictions
  - With this you can now validate the model by analyzing the: accuracy score, classification report results, and confusion matrix

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
From sklearn we use the following functions:
  - Logistic Regression
  - train_test_split
Our supporting library such as metrics allows us to use the following tools:
  - Balanced accuracy score
  - confusion matrix
  - classification report

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

- Balanced Accuracy Score: 0.95
- Accuracy Score: 0.99
- Precision: Class 0 - 1.00, Class 1 - 0.85
- Recall: Class 0 - 0.99, Class 1 - 0.91

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

Overall our trained model seems to predict the true positive outcomes well for the healthy loan class with a precision of 1 and a recall of 0.99. So both the predicted outcomes were true positive and all the values predicted were true positive. However, with our high-risk loans, we obtained a precision of 0.85 and a recall of 0.91. This in translation shows that our model has a tendency of preidcting false positives while also not obtaining all the true positives we prefer.

However, with an accuracy score of 0.99 we can be confident that our model predicts the possible true positive results well.