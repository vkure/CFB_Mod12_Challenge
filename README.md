# CFB Module 12 Challenge
# Credit Report

## Overview

The goal of the challenge is to build a machine learning model to determine the credit-worthiness of borrowers.  Due to the fact that the credit data is very imbalanced (very few risky loans), a re-sampling of data allows for a more accurate model.  The purpose of the analysis is to compare and evaulate the logistic regression models trained with the original and re-sampled data.

The financial information was based on loans for borrowers.  The features for each loan included:  loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, deragotary marks, and total_debt.

The variable to predict is whether an inputted loan would remain healthy or be at risk of default; this was a binary output.  The data set had 75036 healthy loans and 2500 risky loans, so the proportion of risky loans is very low.

The analysis had several steps:
* splitting the data into training and testing sets
* creating a logistic regression model with the original data and generating test statistics
* oversampling to create a balanced data set
* fitting a new logistic regression model with the re-sampled data and generating test statistics
* comparing the test statistics of the two models

The machine learning models were based on logistic regression.

The re-sampling method utilized was random oversampling.

## Results

* Machine Learning Model 1:
    * Accuracy: 0.91 Healthy and 0.90 Risky
    * Precision: 1.00 Healthy and 0.85 Risky
    * Recall: 0.99 Healthy and 0.91 Risky

* Machine Learning Model 2 (Re-Sampled Data):
    * Accuracy: 0.99 Healthy and 0.99 Risky
    * Precision: 1.00 Healthy and 0.84 Risky
    * Recall:  0.99 Healthy and 0.99 Risky


## Summary

 The model fit with re-sampled data (Model 2) had better performance than the model fit with the original data (Model 1).  This is first supported by the fact that Model 2 had an accuracy score of 0.99, compared to 0.91 for Model 1.  Secondly, there is an extra importance placed on correctly identify risky borrowers because that is where potential losses might occur.  In this case, Model 2 had a much higher recall for risky borrowers. 

 While Model 1 had a slightly higher precision, a lower precision for Model 2 would only result in a small amount of missed business.  However, the much higher recall of Model 2 would prevent costly losses from lending to potentially defaulting borrowers.  

 ## Technology

 This analysis requires the use of the following packages:

 