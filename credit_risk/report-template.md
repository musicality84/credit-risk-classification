# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.



	The purpose of this analysis was to train a machine learning model to predict a client's loan risk as either healthy or high risk.  The data included factors typically included in credit score reporting, including each client's loan risk status.  The loan risk status is the value that we are teaching the model to predict, which is listed in the data as loan_status.  In order to train the model to predict these values, we had to separate the loan_status column from the rest of the data and then split the data into training data and testing data.  From there we fit the data to a logistic regression model. Then we were able to compare the results to the testing data to evaluate how well the model did.

 - Accuracy:  The overall accuracy was 99%, which is very good
 - Precision: The precision was 100% for low risk loans, and 85% for high risk loans.  These scores are quite good overall, but it looks like the model may have classified some loans as high risk that are actually low risk.  If we use this model to predict loan risk, we would risk putting off customers who should be able to obtain a loan.
 - Recall: Recall was 99% for low risk loans, and 91% for high risk loans.  These are reasonably good scores.

I would argue that it is more important to be able to identify high risk loans than low risk ones.  However, the model that predicted the low risk loans performed so much better that I would likely recommend that model.