# Module 12 Report

## Overview of the Analysis

In this section, I will describe the analysis I completed for the machine learning models used in this Challenge:

* Purpose: The purpose of this analysis was to build a machine learning model to predict credit risk. By accurately predicting credit risk, we can help financial institutions make informed decisions about lending.
* The data used in this analysis contained various financial information about borrowers, such as their income, credit history, and loan amount. The target variable we were trying to predict was whether the borrower is a high risk or low risk for loan repayment.
*  The target variable is binary, with 'high_risk' and 'low_risk' as possible values. You can use the value_counts function to get a count of each class in the target variable.
* The machine learning process involved several stages. First, we preprocessed the data, which included cleaning the data, handling missing values, and encoding categorical variables. Next, we split the data into a training set and a test set. We then trained several models on the training data and evaluated their performance on the test data. Finally, we selected the best performing model based on its balanced accuracy score and F1 score.
* We used the Logistic Regression algorithm to build our predictive model. To handle the imbalance in our target variable, we also used an oversampling method to increase the number of 'high_risk' instances in our training data. This helped improve the model's ability to identify 'high_risk' borrowers.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
Balanced Accuracy Score: 0.9520479254722232

Confusion Matrix: 
[[18663   102]
 [   56   563]]

Classification Report: 
              precision    recall  f1-score   support

   high_risk       1.00      0.99      1.00     18765
    low_risk       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384


* Machine Learning Model 2:
Accuracy Score: 0.9936781215845847

Confusion Matrix: 
[[18649   116]
 [    4   615]]

Classification Report: 
              precision    recall  f1-score   support

   high_risk       1.00      0.99      1.00     18765
    low_risk       0.84      0.99      0.91       619
...
   macro avg       0.92      0.99      0.95     19384
weighted avg       0.99      0.99      0.99     19384

## Summary

* The oversampled model using Logistic Regression seems to perform the best. This is evident from its higher balanced accuracy score (0.994 vs 0.952) and better recall for the 'low_risk' class (0.99 vs 0.91) compared to the first model. The f1-score for the 'low_risk' class also improved in the oversampled model (0.91 vs 0.88), indicating a better balance between precision and recall
* The performance of a model does depend on the problem we are trying to solve. In this case, if it's more important to predict the 'high_risk' borrowers (the 1s), then a model with a higher recall for the 'high_risk' class would be preferred. On the other hand, if it's more important to correctly identify 'low_risk' borrowers (the 0s), then a model with a higher precision for the 'low_risk' class would be preferred. In this case, the oversampled model performs better at identifying both 'high_risk' and 'low_risk' borrowers.

Given these results, I would recommend the oversampled model. It not only has a higher overall performance, but it also does a better job of identifying 'low_risk' borrowers, which could be particularly important for a lending institution.