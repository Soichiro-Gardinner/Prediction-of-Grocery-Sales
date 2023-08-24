# Sales Prediction Interpretability Study

This repository focuses on interpreting the predictions of a sales forecasting machine learning model. By employing both SHAP and LIME, two popular model interpretability techniques, we aim to provide insights into the decision-making process of the model.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Preprocessing and Cleaning](#data-preprocessing-and-cleaning)
- [Model Development and Training](#model-development-and-training)
- [Model Interpretability](#model-interpretability)
- [Visual Interpretations](#visual-interpretations)
- [How to Use](#how-to-use)

## Project Overview

In today's data-driven world, while accurate predictions are important, understanding the reasoning behind those predictions is equally crucial. This project uses the `sales_predictions.csv` dataset to train a machine learning model and then employs interpretability techniques to break down the predictions.

## Data Preprocessing and Cleaning

**Key Steps:**

1. **Loading the Data:** We begin by loading the sales data.
2. **Anomaly Handling:** Certain anomalies in the `Item_Fat_Content` are addressed.
3. **Feature Selection:** The `Item_Identifier` and `Item_Outlet_Sales` features are dropped, keeping the rest for training.
4. **Preprocessing Pipeline:** A comprehensive pipeline is established to handle both numerical and categorical variables. This pipeline takes care of missing values and scales or encodes features as necessary.

## Model Development and Training

- **RandomForestRegressor:** This ensemble learning method is used for sales prediction due to its versatility and robustness.
- **Train-Test Split:** Data is split into training and testing sets to ensure that the model's performance is evaluated on unseen data.
- **Model Training:** The preprocessed training data is used to train the RandomForest model.

## Model Interpretability

**Approaches Used:**

- **SHAP (SHapley Additive exPlanations):** It breaks down the prediction for a single instance and provides insights into the impact of different features.
- **LIME (Local Interpretable Model-agnostic Explanations):** This method offers a local interpretation of model predictions by approximating the model using an interpretable one.

## Visual Interpretations

The visual results of the interpretability techniques are saved as images and can be found in the "Project 1[Revisited]" folder:

### LIME Interpretations:
- **Low Sales LIME Interpretation:** 
![Low Sales LIME](Project%201[Revisited]/low_sales_lime.png)

- **High Sales LIME Interpretation:** 
![High Sales LIME](Project%201[Revisited]/high_sales_lime.png)

### SHAP Interpretations:
- **Low Sales SHAP Interpretation:** 
![Low Sales SHAP](Project%201[Revisited]/low_sales_shap.png)

- **High Sales SHAP Interpretation:** 
![High Sales SHAP](Project%201[Revisited]/high_sales_shap.png)

## How to Use

1. **Clone the Repository:** Start by cloning this repository to your local machine.
2. **Install Necessary Libraries:** Ensure you have all required Python libraries installed. They can be found at the beginning of the notebook.
3. **Run the Notebook:** Open the provided notebook for an in-depth, step-by-step walkthrough of every stage of this project, from data preprocessing to model interpretation.
4. **View Visuals:** Navigate to the "Project 1[Revisited]" folder to see the visual interpretations of model predictions.

Enjoy exploring the intricacies of sales prediction interpretation!

