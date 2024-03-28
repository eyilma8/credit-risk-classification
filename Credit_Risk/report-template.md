# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

The analysis is to review various data that includes loan_size, interest_rate, borrower_income,	debt_to_income,	num_of_accounts	derogatory_marks,	total_debt,	loan_status to determine credit worthiness
* Explain what financial information the data was on, and what you needed to predict.
The financial information are as detailed above, and the task is to predict credit score which means credit worthiness

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The attemp it to predict the loan status agains all othee financial information provided

* Describe the stages of the machine learning process you went through as part of this analysis.

data preprocess, train and test and predict
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

I used logistic regression method to predict

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.

The accuracy score is 0.9924164259182832 and 


Results
•	Accuracy:  0.9924
•	Balanced Accuracy: 0.95205
•	Precision
o	Healthy: 1.00
o	High-Risk: 0.87
•	Recall
o	Healthy: 0.99
o	High-Risk: 0.94


## Summary

The Logistic Regression model does a very good job predicting healthy loans. However, according to the test data, it classifies 10% of high-risk loans as healthy. While none of the loans used for training are for very large amounts of money (all are less than 24,000), a loan that defaults, especially early in its term, could cost the company more than the interest earned from many healthy loans.
There are also very few high-risk loans for the model to learn from when compared to the number of healthy loans in the data set. If more of these types of loans could be added to the data to train from, there may be improvement to the model.
For trying to classify loans, trying to prevent high-risk loans is more important than giving out a loan as more money can be lost from a single loan that defaults than the interest earned from a loan.
Model Pros and Cons
Pros
•	Healthy loan prediction is excellent
•	Lots of data points for healthy loans
Cons
•	Very few high-risk loan data points
•	Loans are only in value up to $24,000
•	About 10% of high-risk loans are classified as healthy
If this model is only used for loans less than $24,000 and historically the bank has had healthy loans to risky loans equal to the fraction seen in the data (30 to 1) then I would say the model may be adequate, otherwise I would not recommend it due to increasing risk. Furthermore, this model gives out binary answers (healthy/risky), with no percentage to allow for a more detailed review for loans on the edge of a decision.