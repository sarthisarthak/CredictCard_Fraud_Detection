# Credit Card Fraud Detection using Machine Learning

This project aims to detect fraudulent credit card transactions using machine learning techniques. The model was trained on an imbalanced dataset of credit card transactions, and it achieved an accuracy of 91%. The goal is to build a robust model that can help financial institutions reduce losses due to fraudulent activities.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Model](#model)
- [Results](#results)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

Credit card fraud detection is a significant challenge for financial institutions. This project focuses on detecting fraudulent transactions using various machine learning algorithms. Due to the highly imbalanced nature of the dataset, where only a small fraction of transactions are fraudulent, special techniques like oversampling and under-sampling were applied to improve the model's performance.

**Key Features:**

- Preprocessing of imbalanced data
- Multiple machine learning models evaluated
- Achieved 91% accuracy on test data
- Performance metrics include precision, recall, F1-score, and ROC-AUC score

## Dataset

The dataset used in this project is the [Credit Card Fraud Detection dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud) from Kaggle. It contains 284,807 transactions, of which 492 are fraudulent. The dataset is highly imbalanced, with only 0.172% of transactions being fraudulent.

**Features:**

- 30 numerical features including `Time`, `Amount`, and `V1` to `V28`, which are the result of PCA transformation.
- The target variable `Class`, where `1` indicates fraud and `0` indicates a valid transaction.

## Model

Several machine learning models were tested to identify fraudulent transactions. The model achieving the highest accuracy of 91% was a Random Forest classifier. Data preprocessing steps included:

- **Data Scaling**: StandardScaler was used to normalize the `Amount` and `Time` features.
- **Handling Imbalance**: The `SMOTE` technique was used to oversample the minority class (fraudulent transactions).
- **Feature Selection**: Recursive feature elimination (RFE) was applied to select the most important features.

**Models evaluated:**

- Logistic Regression
- Decision Trees
- Random Forest (best performing)
- Gradient Boosting
- Support Vector Machine (SVM)

## Results

The Random Forest model achieved the following performance metrics on the test set:

- **Accuracy**: 91%
