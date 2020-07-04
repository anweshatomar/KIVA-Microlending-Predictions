# Kiva-Loan-Dataset

## BREIF DESCRIPTION:

Kiva.org is an online crowdfunding platform to extend financial services to poor and financially excluded people around the world, the dataset was downloaded from Kaggle for the past two years.

The aim is to apply machine learning methods to gain insight into how Kiva determines the amount (USD) and repayment interval type (monthly, bullet, or irregular) of each loan. 

Kiva provides features such as the number of lenders, borrower's gender(s), loan use activity, and more. 

In this project, we built models to predict the loan amount (regression) and the repayment interval type (classification) and multitarget prediction(repayment_interval, activities). 

Hyperparameter tuning was performed over different models (Logistic Regression, Random Forest, Decision Trees, Hgbc, Xgboost, and Multilayer Perceptron).

This information can inform both lenders and borrowers in the Kiva crowdfunding process. 


## TOP FINDINGS: 

- The target for regression is 'loan_amount', the regression models were not very powerful predictive models based on their accuracy. 
- The MLP regressor was the best amongst the other two (Decision Tree and Random Forest).
- The classification model predicting repayment interval type, the results reveal the best model to be Histogram Gradient Boosting with an F1 score of 0.874. 
 
