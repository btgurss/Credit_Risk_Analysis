# Credit_Risk_Analysis

## Overview
In this project, I was tasked with finding a machine learning model for a credit card risk data set.  The goal was to see if, by inputting the data into different learning models,  we could come up with an efficient and accurate way of predicting which consumers were most at risk of defaulting on loans.  I ran through numerous models to determine if there were any models that could successfully predict high risk loans and then determined which of these models did the best job.  A list of the different machine learning models is below:

- RandomOverSampler
- SMOTE OverSampler
- Cluster Centroids Undersampling
- SMOTEENN Over/Under Sampling combination
- Balanced Random Forest Classifier
- AdaBoostClassifier

In order to get better results I manipulated the data in the following ways before running the machine learning algorithms
- In the 4 models that included over/Under sampling I chosea set of features to run on.  In the classifiers I began with every column or feature in the list
- Next, I scaled the data to eliminate large numbers skewing the learning model
- I then found the important features of the dataset so that I could narrow my model to fewer columns/features

## Results
For each learning model that was used the following information was extracted.
- A balanced accuracy score was used to determine how often the model made the correct prediction
- A confusion matrix was created to show the number of True/False positives and negatives
- A classification report was created to show the precision, sensitivity, and f1 score of the model

Here are the results for each model:

### Random OverSampler
![Random_OverSampling.png](Images/Random_OverSampling.png)
- Accuracy Score: 62%   This tells us that the model correctly predicted the outcome 62% of the time.
- Precision: .01 for predicting high risk loans and 100% for predicting low risk loans.  These numbers tell very differenct stories.  First, it tells us the model predicted a lot of high risk loans that were not actually high risk (this is the .01 number).  The model also, however, was very good at predicting loans that were low risk as it was correct almost 100(This was rounded up from 99.6) percent of the time.
- Sensitivity: .72 and .52.  This tells us that of the high risk loans in the data set, the model predicted high or low correctly 72 percent of the time.  On the other hand, the model was only successful at correctly predicting the low risk loans 52 percent of the time.

### SMOTE OverSampler
![SMOTE.png](Images/SMOTE.png)
- Accuracy Score: 61%   This tells us that the model correctly predicted the outcome 61% of the time.
- Precision: .01 for predicting high risk loans and 100% for predicting low risk loans.  These numbers tell very differenct stories.  First, it tells us the model predicted a lot of high risk loans that were not actually high risk (this is the .01 number).  The model also, however, was very good at predicting loans that were low risk as it was correct almost 100(This was rounded up from 99.6) percent of the time.
- Sensitivity: .67 and .55.  This tells us that of the high risk loans in the data set, the model predicted high or low correctly 67 percent of the time.  On the other hand, the model was only successful at correctly predicting the low risk loans 55 percent of the time.

### Cluster Centroids Undersampling
![UnderSampling.png](Images/UnderSampling.png)
- Accuracy Score: 61%   This tells us that the model correctly predicted the outcome 61% of the time.
- Precision: .01 for predicting high risk loans and 100% for predicting low risk loans.  These numbers tell very differenct stories.  First, it tells us the model predicted a lot of high risk loans that were not actually high risk (this is the .01 number).  The model also, however, was very good at predicting loans that were low risk as it was correct almost 100(This was rounded up from 99.7) percent of the time.
- Sensitivity: .78 and .40.  This tells us that of the high risk loans in the data set, the model predicted high or low correctly 78 percent of the time.  On the other hand, the model was only successful at correctly predicting the low risk loans 40 percent of the time.

### SMOTEENN Over/Under Sampling combination
![SMOTEENN.png](Images/SMOTEENN.png)
- Accuracy Score: 59%   This tells us that the model correctly predicted the outcome 59% of the time.
- Precision: .01 for predicting high risk loans and 100% for predicting low risk loans.  These numbers tell very differenct stories.  First, it tells us the model predicted a lot of high risk loans that were not actually high risk (this is the .01 number).  The model also, however, was very good at predicting loans that were low risk as it was correct almost 100(This was rounded up from 99.7) percent of the time.
- Sensitivity: .73 and .48.  This tells us that of the high risk loans in the data set, the model predicted high or low correctly 73 percent of the time.  On the other hand, the model was only successful at correctly predicting the low risk loans 48 percent of the time.

### Balanced Random Forest Classifier
![RandomForest.png](Images/RandomForest.png)
- Accuracy Score: 79%   This tells us that the model correctly predicted the outcome 79% of the time.
- Precision: .03 for predicting high risk loans and 100% for predicting low risk loans.  These numbers tell very differenct stories.  First, it tells us the model predicted a lot of high risk loans that were not actually high risk (this is the .03 number).  The model also, however, was very good at predicting loans that were low risk as it was correct almost 100(This was rounded up from 99.6) percent of the time.
- Sensitivity: .70 and .87.  This tells us that of the high risk loans in the data set, the model predicted high or low correctly 70 percent of the time.  On the other hand, the model was only successful at correctly predicting the low risk loans 87 percent of the time.

### AdaBoostClassifier
![AdaBoost.png](Images/AdaBoost.png)
- Accuracy Score: 69%   This tells us that the model correctly predicted the outcome 69% of the time.
- Precision: .88 for predicting high risk loans and 100% for predicting low risk loans.  This tells us that when the model predicted that a loan would be high risk, it was correct 88% of the time.  The model also, however, was very good at predicting loans that were low risk as it was correct almost 100(This was rounded up from 99.6) percent of the time.
- Sensitivity: .38 and 1.00.  This tells us that of the high risk loans in the data set, the model predicted high or low correctly 38 percent of the time.  On the other hand, the model was only successful at correctly predicting the low risk loans almost 100 percent of the time.

## Summary
When determining which model to run the data in I think a few things need to be considered.  If the goal is to make sure deserving patrons receive loans (meaning we correctly predict low risk group), then the AdaBoost Classifier is the best model.  There were very few low risk loans that were predicted to be high risk.  If the goal is to make sure we catch as many high risk loans as possible, any of the other models do a better than average job.  Overall, the best model might be the BalancedRandomTree Classifier.  It still has a decent number of low risk loans that were predicted as high risk, but this number is much lower than any of the over/under sampling models.  It also does a much better job of predicted the high risk than the AdaBoost model.

My Suggestions:
- AdaBoost if we want to make sure low risk groups are marked correctly
- BalancedRandomTree if we want to catch as many high risk as possible while still getting some low risk correct as well.
