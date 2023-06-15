# Bank Customer Churn Analysis

This repository contains code for analyzing and predicting customer churn in a bank. The dataset used for this analysis is provided in the `Bankchurner.csv` file.

## Overview

The goal of this project is to analyze customer churn in a bank and develop predictive models to identify customers who are likely to churn. The code provided performs various steps of the analysis, including data import, outlier detection, correlation analysis, and model building.

## Usage

1. Import the required libraries:
   - pandas
   - numpy
   - seaborn
   - matplotlib.pyplot
   - sklearn.preprocessing.MinMaxScaler
   - sklearn.model_selection.train_test_split
   - sklearn.preprocessing.StandardScaler
   - sklearn.ensemble.RandomForestClassifier
   - sklearn.neighbors.KNeighborsClassifier
   - sklearn.ensemble.AdaBoostClassifier
   - sklearn.metrics.accuracy_score

2. Import the dataset:
   - Use `pd.read_csv('Bankchurner.csv')` to load the dataset into a pandas DataFrame.

3. Data preprocessing:
   - Drop irrelevant columns using `df.drop()`.
   - Create a numeric-only DataFrame using `df.select_dtypes()`.
   - Detect outliers using the `detect_outliers_by_row()` function.
   - Normalize the numeric DataFrame using `sklearn.preprocessing.MinMaxScaler`.

4. Correlation analysis:
   - Calculate the correlation matrix using `normalized_df.corr()`.
   - Visualize the correlation heatmap using `seaborn.heatmap()`.

5. Model building:
   - Drop unnecessary columns and encode categorical variables using `pd.get_dummies()`.
   - Split the data into training and testing sets using `train_test_split()`.
   - Apply feature scaling using `sklearn.preprocessing.StandardScaler`.
   - Train and evaluate different models:
     - Random Forest: `sklearn.ensemble.RandomForestClassifier`
     - K-Nearest Neighbors: `sklearn.neighbors.KNeighborsClassifier`
     - AdaBoost: `sklearn.ensemble.AdaBoostClassifier`

## Results

The accuracy scores of the implemented models on the test data are as follows:
- Random Forest: 86.04%
- K-Nearest Neighbors: 82.92%
- AdaBoost: 84.8%

## Conclusion

This project demonstrates the process of analyzing customer churn in a bank and building predictive models to identify potential churners. The implemented models can be further optimized and tuned for better performance.

