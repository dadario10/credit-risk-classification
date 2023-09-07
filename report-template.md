# Module 20 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
 - the purpose of this analysis is to assess the risk, either healthy or high risk, of providing clients with loans

* Explain what financial information the data was on, and what you needed to predict.
 - the data is based on loan size, interest rates, borrower income, debt to income ration, number of accounts per customer, derogatory marks, total debt, and loan status.

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
 - Split the data into labels using the loan status
 - `value_counts` was used to check the balance of the target values.
 - Split the data into training and testing datasets by using `train_test_split`
 - Create a Logistic Regression Model with the Original Data
 - Save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model
 - Predict a Logistic Regression Model with Resampled Training Data
 - Use the `LogisticRegression` classifier and the resampled data to fit the model and make predictions
 - Evaluate the model's performance

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
   - Accuracy: 0.9918489475856377
   - Precision: 
    - Healthy 1.00
    - High risk 0.85
   - Recall: 
    - Healthy 0.99
    - High risk 0.91

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  - Accuracy: 0.9947308560359689
   - Precision: 
    - Healthy 0.99
    - High risk 0.99
   - Recall: 
    - Healthy 0.99
    - High risk 0.99

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

 - Based on the final results, model 1 shows healthy loan prediction at 100% and high risk loan at 85%. Model 2 shows healthy loan prediction at 99% and high risk loan at 99%. Although model 1 has a 100% healthy loan prediction, I believe model 2 is the better choice. You lose 1% on the healthy loan but you only lose 1% on high risk as well. Model 1 has 15% missed on high risk, thats 15% of business that this organization could have profitted on. Therefore the 1% loss on healthy loan from model 1 is worth the 14% gain compared to the other model on high risk loans. To summarize, I believe that model 2 is the better option for this company to use as it will result in more loan profits.