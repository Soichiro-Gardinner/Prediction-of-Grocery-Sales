# Project 1 - Revisited

## Introduction

In this project, we revisit the task of predicting supermarket sales using the updated tools in sklearn v1.2. We apply what we've learned to explain how our models make their predictions. The goal is to create a new version of our final project notebook, including explanations of the models, feature importances, SHAP analysis, and coefficients, as well as serializing the best models for future use.

## Table of Contents

1. Installation
2. Data
3. Data Preprocessing
4. Linear Regression
   - Coefficients
   - Top 3 Most Impactful Features
5. Random Forest Regressor
   - Feature Importances
   - Top 5 Most Important Features
6. SHAP Analysis
   - SHAP Summary Plot
   - Interpretation of Top Features
7. Serialization
   - Best Models
8. Conclusion

## Installation

To run the code and reproduce the results, you need to have the following libraries installed:

- pandas
- matplotlib
- scikit-learn
- shap

## Data

The dataset used for this project is "sales_predictions.csv." It contains information about various products in a supermarket and their corresponding outlet sales. The task is to predict the sales of products based on different features.

## Data Preprocessing

Before building our models, we perform data preprocessing to handle inconsistencies in categorical data, drop unnecessary columns, and split the dataset into features (X) and target (y). We also create a preprocessing pipeline using ColumnTransformer to handle numerical and categorical features separately.

## Linear Regression

### Coefficients

We start by fitting a Linear Regression model using the preprocessed data. We then extract and visualize the coefficients determined by the model to understand the impact of each feature on the target variable.

### Top 3 Most Impactful Features

From the coefficients plot, we identify the top 3 most impactful features in our Linear Regression model and interpret their coefficients in plain English.

## Random Forest Regressor

We also use a Tree-Based model, specifically the Random Forest Regressor, to predict supermarket sales.

### Feature Importances

We fit the Random Forest Regressor using the preprocessed data and extract the feature importances to understand which features contribute the most to the model's predictions.

### Top 5 Most Important Features

From the feature importances, we identify the top 5 most important features in our Random Forest Regressor and discuss their significance.

## SHAP Analysis

To gain deeper insights into our models, we use SHAP analysis to understand how each feature affects individual data points' predictions. We create a SHAP summary plot to visualize the impact of each feature on the model's predictions.

### Interpretation of Top Features

From the SHAP summary plot, we interpret the top features that have the highest impact on the model's predictions. We explain the direction of their impact (positive or negative) and how changes in these features influence the sales predictions.

## Serialization

To ensure we can use our best models and SHAP analysis in future assignments or projects, we serialize and save them using the joblib library.

### Best Models

We serialize the following best models:

- Preprocessing ColumnTransformer
- Linear Regression Model
- Random Forest Regressor Model

The serialized models are saved in "best-models.joblib".

## Conclusion

In this project, we revisited the task of predicting supermarket sales and applied various machine learning models. We explored the coefficients of the Linear Regression model, the feature importances of the Random Forest Regressor, and the SHAP values to gain insights into the models' predictions. The best models and SHAP analysis are serialized for future use.

For more details, please refer to the Jupyter Notebook "Project 1 - Revisited.ipynb" in this repository.
