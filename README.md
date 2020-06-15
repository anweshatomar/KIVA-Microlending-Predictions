# Kiva-Loan-Dataset

## Introduction and Goal:

Kiva.org is an online crowdfunding platform to extend financial services to poor and financially excluded people around the world, the dataset was downloaded from Kaggle for the past two years.

The aim is to apply machine learning methods to gain insight into how Kiva determines the amount (USD) and repayment interval type (monthly, bullet, or irregular) of each loan. 

The data was subset based on Latin American countries out of personal interest and to narrow our focus.

 Kiva provides features such as the number of lenders, borrower's gender(s), loan use activity, and more. 

In this project, we built models to predict the loan amount (regression) and the repayment interval type (classification) and multitarget prediction(repayment_interval, activities). 

This information can inform both lenders and borrowers in the Kiva crowdfunding process. 


## Pre-Processing:

The multidimensionality poverty index CSV file was merged with the loan dataset, Then the activities and counties were grouped together in order to reduce the dimensionality. Feature engineering was performed to obtain the gender count. Since all the missing values were under 20 per cent we then dropped all the missing values. 



## Machine Learning Models:

### Regression: 

The target for regression is 'loan_amount'. The regression models were not very powerful predictive models based on their accuracy. The MLP regressor was the best amongst the other two (Decision Tree and Random Forest). There are likely many reasons why this is a poor model for predicting loan amount, but we speculate that nature of the features we chose are not great indicators of the Latin American Kiva loan amounts under the given parameters.


### Classification:

The classification model predicting repayment interval type, the results reveal the best model to be Histogram Gradient Boosting with an F1 score of 0.874. Thus, this is quite a good model based on the F1 score. Additionally, the next best models, Random Forest, and Multilayer Perception Classification both performed well with F1 scores above 0.80. According to our Random Forest Classifier, the top 5 features given in order of importance are Loan Term (months), Country Colombia, Loan Amount, Agriculture and Livestock Activity, and MPI. Interestingly, Colombia has more predictive power than other Latin American countries (importance of 0.0986365). If we recall some of our EDA plots, Colombia received the 3rd highest number of loans in Latin America and it was highly (negatively) correlated with repayment interval, our target. Agriculture and livestock is the second highest activity in Latin America and is also negatively correlated to the repayment interval. MPI is the 5th most important at a value of 0.0824386, indicates that poverty level is playing an important role in Kiva loan activity.


### Multitarget classification and prediction:

For multitarget prediction, both target variables were encoded. The K nearest neighbour and Random Forest classifier were used to for classification and prediction. Next user input for each of variable is taken and predict the repayment interval and activity of that loan. 
