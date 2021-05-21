# Classification - Risky Business

## Background

Auto loans, mortgages, student loans, debt consolidation ... these are just a few examples of credit and loans that people are seeking online. Peer-to-peer lending services such as LendingClub or Prosper allow investors to loan other people money without the use of a bank. However, investors always want to mitigate risk, so you have been asked by a client to help them use machine learning techniques to predict credit risk.

### Part 1: Resampling

Use the imbalanced learn  library to resample the LendingClub data and build and evaluate logistic regression classifiers using the resampled data by:

1. Load the Lending Club data, split the data into training and testing sets, and scale the features data.
2. Oversample the data using the `Naive Random Oversampler` and `SMOTE` algorithms.
3. Undersample the data using the `Cluster Centroids` algorithm.
4. Over- and under-sample using a combination `SMOTEENN` algorithm.

Research Questions:

- Which model had the best balanced accuracy score?
- Which model had the best recall score?
- Which model had the best geometric mean score?

### Part 2: Ensemble

Train and compare two different ensemble classifiers to predict loan risk and evaluate Easy Ensemble Classifier and Balanced Random Forest models by:

1. Load the Lending Club data, split the data into training and testing sets, and scale the features data.
2. Train the model using the quarterly data from LendingClub provided in the `Resource` folder.
3. Calculate the balanced accuracy score from `sklearn.metrics`.
4. Print the confusion matrix from `sklearn.metrics`.
5. Generate a classification report using the `imbalanced_classification_report` from imbalanced learn.
6. For the balanced random forest classifier only, print the feature importance sorted in descending order (most important feature to least important) along with the feature score.

Research Questions:

- Which model had the best balanced accuracy score?
- Which model had the best recall score?
- Which model had the best geometric mean score?
- What are the top three features?


### Files

[Resampling Notebook](Analysis/credit_risk_resampling.ipynb)

[Ensemble Notebook](Analysis/credit_risk_ensemble.ipynb)

[Lending Club Loans Data](Data/LoanStats_2019Q1.csv.zip)

## Summary of Results

### Resampling

1.) Which model had the best balanced accuracy score?

Oversample: 0.653 - best balanced accuracy score 
SMOTE: 0.647
Undersample: 0.566
SMOTEEN: 0.652

2.) Which model had the best recall score?

Oversample: 0.61 
SMOTE: 0.67 - best recall score
Undersample: 0.56
SMOTEEN: 0.57

3.) Which model had the best geometric mean score?

Oversample, SMOTE and SMOTEEN models had the same geo scores:

Oversample: 0.65 
SMOTE: 0.65
Undersample: 0.57
SMOTEEN: 0.65


### Ensemble Learning

1.) Which model had the best balanced accuracy score?

BalancedRandomForestClassifier: 0.729
EasyEnsembleClassifier: 0.931 - best balanced accuracy score

2.) Which model had the best recall score?

BalancedRandomForestClassifier: 0.84
EasyEnsembleClassifier: 0.94 - best recall score

3.) Which model had the best geometric mean score?

BalancedRandomForestClassifier: 0.72
EasyEnsembleClassifier: 0.93 - best geo score

4.) What are the top three features?

(0.07646711017201446, 'total_rec_prncp')
(0.0681731200022894, 'last_pymnt_amnt')
(0.05699252404641979, 'total_pymnt')
