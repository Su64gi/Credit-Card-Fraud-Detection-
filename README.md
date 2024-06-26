# Credit-Card-Fraud-Detection

![Python](https://img.shields.io/badge/Python-3.8.10-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-LightGBM-orange)
![Tuning](https://img.shields.io/badge/Tuning-Optuna-red)
![Deployment](https://img.shields.io/badge/Dashboard-Plotly-purple)

## Introduction
It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase.

## Problem Statement
With the provided information, build a model to predict whether this customer will commit fraud when using a credit card or not.

## Description
This data set is [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) from Kaggle. The dataset contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

### Exploratory Data Analysis
* Due to security issues, the original features V1, V2, ... V28 have been modified by PCA. However, we can guess that these features could be credit card number, expiration date, CVV, cardholder name, transaction location, transaction datetime, etc.
The only two features that have not been converted with PCA are Time and Amount. Therefore, we only need to focus on processing these two features

### Data Preprocessing
* Log transform amount feature
* Handling Data Imbalance: I used *SMOTE* method for balancing the dataset. 
* *Robust scaling* all data

### Features Selection:
* On using *Pearsonr Correlation* method, I don't need to drop any features.

### Model Training

#### Training lists
* Widely used ML models: Logistic Regression, Decision Tree, Random Forest, LightGBM, Catboost, XGBoost, AdaBoost
#### Amount and Time
![e535217f-46f2-4101-bfc9-1a3905663909](https://github.com/Su64gi/Credit-Card-Fraud-Detection-/assets/155756162/ddeabadc-5071-42ba-9c66-77e7c54f4011)

#### Training set and validation set
![9101820 (2)](https://github.com/Su64gi/Credit-Card-Fraud-Detection-/assets/155756162/263b1c7c-ebf8-411d-bcac-774bbbfbf6f1)

#### precision-recall curve

![6e452621-6def-48fd-9e90-c9884181c452](https://github.com/Su64gi/Credit-Card-Fraud-Detection-/assets/155756162/73fa512a-6934-4fc3-8def-08f4578842aa)
