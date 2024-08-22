# credit-risk-classification
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.


## Overview of the Analysis
Reference for live code and text narrative saved to [credit_risk_classification.ipynb](https://github.com/Kre8iveEnvy/credit-risk-classification/blob/main/credit_risk_classification.ipynb)

* The purpose of this ananlysis is to build a model that can identity the creditworthiness of borrowers.

* The provided data [lending_data.csv](https://github.com/Kre8iveEnvy/credit-risk-classification/blob/main/Resources/lending_data.csv) is a csv file that includes the following financial which will be used to test and predict the outcome of a healthy loan vs a high-risk loan
    - loan_size 
    - interest_rate
    - borrower_income
    - debt_to_income
    - num_of_account
    - derogatory_marks
    - total_debt
    - loan_status

* The first step was to separate the data into labels and features, labels being the loan_status and features being the behavior data such as loan size, interest rate, income, etc. The data has a row count of 75,036 with 97% (75,036) of loan_status equal to 0 indicating healthy loan and 3% (2,500) of loan_status equal to 1 indicating high-risk loan.

* The data was then split into a training (75%split) and testing (25%split) dataset using the method of train_test_split and then fitted into a logistic regression model using the training data. The initial model had a Training Data Score of 0.9914 and a Testing Data Score of 0.9924. 

* The final step was to evaluate the models performnce by saving the predictions on the testing data (25% of total which is 19,384) using the testing feature data and the fitted model. The confusion matrix showed a 96%(18,679) TruePositive, 3% TrueNegative(558), and 1% being the combination of FalseNegative(67) and FalsePositive(80). 


## Results

Using the classification report for the model there was an F1-score of 99% for accuracy.The logistice regression model received an f1-score of 100% for predicting healthy loans and 88% f1-score at predicting high rick loans.

* See below image for the breakdown of Healthy Loans (0) vs High Risk Loans (1) 
![classification_report](https://github.com/Kre8iveEnvy/credit-risk-classification/blob/main/classification_report.png)




