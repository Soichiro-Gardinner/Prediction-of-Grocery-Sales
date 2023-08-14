# Sales Predictions Model Explanations

This repository contains code and examples for explaining predictions made by a sales predictions model. The explanations are generated using two different techniques: SHAP (SHapley Additive exPlanations) and LIME (Local Interpretable Model-agnostic Explanations).

## Table of Contents

- [Overview](#overview)
- [Data](#data)
- [Getting Started](#getting-started)
- [Explanation Techniques](#explanation-techniques)
- [Examples](#examples)
- [License](#license)

## Overview

In this repository, we explore how to explain predictions made by a sales predictions model using SHAP and LIME. We use a random forest regressor model to predict sales based on various features. The goal is to provide local explanations for both high and low sales predictions.

## Data

The data used for training and testing the model is the "Sales Predictions" dataset. This dataset includes various features related to products and outlets, as well as the target variable "Item_Outlet_Sales," which represents the predicted sales.

## Getting Started

To run the code in this repository, follow these steps:

1. Clone the repository to your local machine.
2. Ensure you have the required dependencies installed. You can install them using `pip install -r requirements.txt`.
3. Place the "sales_predictions.csv" file in the repository's root directory.

## Explanation Techniques

We utilize two explanation techniques to understand our sales predictions model:

1. **SHAP (SHapley Additive exPlanations):** SHAP values provide insights into how individual features contribute to a prediction. We use the SHAP library to generate force plots for high and low sales predictions.

2. **LIME (Local Interpretable Model-agnostic Explanations):** LIME creates locally faithful explanations for model predictions. We use the LimeTabularExplainer to explain single observations and visualize the contributions of each feature.

## Examples

We provide examples for both SHAP and LIME explanations:

- SHAP Examples: SHAP force plots are generated for both high and low sales predictions. These plots visualize how individual features impact the predictions.
![SHAP Force Plot - High Sales](high_sales_shap_force_plot.png)
![SHAP Force Plot - Low Sales](low_sales_shap_force_plot.png)

- LIME Examples: LIME explanations are generated for high and low sales predictions using the LimeTabularExplainer. We visualize the contributions of different features to the predictions.
![LIME Explanation - High Sales](high_sales_lime_explanation.png)
![LIME Explanation - Low Sales](low_sales_lime_explanation.png)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

