# Concrete Compressive Strength

A comparison of three algorithms to model the compressive strength of concrete samples

## Introduction

This model is used to analyse the results of an experiment to determine the optimum ingredients for concrete. It actually consists of three models:
-	K Nearest Neighbour Regressor
-	Random Forest Regressor
-	Neural Net with one hidden layer

The predictive performance of each model was measured using a mean absolute percentage error on a separate test set. The relationship between ingredients and compressive strength is known to be highly non-linear. 

## DATA

The data is in the form of a CSV table consisting of 1030 rows and nine columns. Each row of data represents a sample of concrete which was crushed to find its compressive strength. The first seven columns list the ingredients used in each sample of concrete. The eighth column is the number of days the sample was allowed to cure, and the final column is the compressive strength of the sample.

The raw, labelled data is available in a CSV format which can be downloaded from the Data Science Dojo https://code.datasciencedojo.com. It was originally compiled by the department for Civil Engineering, Chung-Hua University.  

## MODEL 

The relationship between the concrete ingredients and the compressive strength is known to be highly non-linear, but I did not want an overly complex algorithm to model the data. I also wanted to discover the key ingredients for making the concrete strong. This is a comparison of three models.

## HYPERPARAMETER OPTIMSATION

The first two models were tuned using a five-fold cross-validated grid search. The third model was tuned manually.

## RESULTS

The performance of each model was based on the mean absolute percentage error, measured on a separate test set.
-	K-nearest neighbour: 67% 
-	Random Forest: 83%
-	Neural Net: 92%

The Neural Net was the most accurate, but the Random Forest was the most interpretable, giving the key ingredients required to increase the concrete’s compressive strength. 

