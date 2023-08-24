# Sales Prediction Interpretability

This repository focuses on interpreting machine learning models built for predicting sales. Using the dataset `sales_predictions.csv`, we constructed machine learning models and then proceeded to explain their predictions using techniques like SHAP and LIME.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Model Training](#model-training)
- [Model Interpretation](#model-interpretation)
- [Visuals](#visuals)
- [How to Use](#how-to-use)

## Overview

Sales predictions are crucial for business strategy, and understanding the factors behind such predictions is equally significant. This project serves this very purpose by not just predicting but also interpreting the predictions.

## Features

The dataset includes various features like `Item_MRP`, `Outlet_Type`, `Item_Visibility`, and more.

## Model Training

- Linear Regression: Used for its simplicity and interpretability.
- Random Forest Regressor: A tree-based model to capture complex patterns in the data.

## Model Interpretation

- **SHAP (SHapley Additive exPlanations)**: Utilized to understand the impact of different features on the predictions of a single instance.
- **LIME (Local Interpretable Model-agnostic Explanations)**: Used to locally interpret model predictions.

## Visuals

### LIME Explanations:
![LIME for Low Sales](low_sales_lime.png)
![LIME for High Sales](high_sales_lime.png)

### SHAP Explanations:
![SHAP for Low Sales](low_sales_shap.png)
![SHAP for High Sales](high_sales_shap.png)

## How to Use

1. Clone the repository.
2. Ensure you have all the required libraries installed.
3. Run the provided code to train models and interpret them.
4. Use the visualization images to understand the interpretability results.
