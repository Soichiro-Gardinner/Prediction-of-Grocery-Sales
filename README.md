# Sales Prediction Interpretability Study

This repository focuses on interpreting the predictions of a sales forecasting machine learning model. By employing both SHAP and LIME, two popular model interpretability techniques, we aim to provide insights into the decision-making process of the model.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Preprocessing and Cleaning](#data-preprocessing-and-cleaning)
- [Model Development and Training](#model-development-and-training)
- [Model Interpretability](#model-interpretability)
- [Visual Interpretations](#visual-interpretations)
- [Interpretation Summary](#interpretation-summary)
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

## Interpretation Summary


### Mean Absolute SHAP Values:
- **Outlet_Establishment_Year**: The establishment year significantly influences predictions with an impact of ~293.2.
- **Item_MRP**: MRP is the next influential feature with an impact of ~256.96.
- **Item_Weight & Item_Visibility**: Both influence predictions with impacts of ~47.61 and ~34.94, respectively.
- Features like many `Item_Identifier` values have negligible influence.

### SHAP Values for the 5th Instance:
- **Item_Weight**: Decreases the prediction by ~18.42 units.
- **Item_Visibility**: Increases the prediction by ~3.19 units.
- **Item_MRP**: Decreases the prediction substantially by ~199.84 units.
- **Outlet_Establishment_Year**: Reduces the prediction by ~183.8 units.

Most other features have minimal influence on this instance.

### Model
We used the Random Forest Regressor as our machine learning model. Following training, a few inconsistencies in the dataset were addressed, and categorical features underwent one-hot encoding.

### Global Interpretability with SHAP

SHAP offers insights into model predictions on an average scale.

1. **Summary Bar Plot:** 
   ![SHAP Summary Bar Plot](Shap%20Summary%20plot.png)
   This plot provides a comprehensive view of features exerting the most significant impact on model predictions. Features receive a ranking based on their importance.
   
2. **Dot Plot:** 
   ![SHAP Dot Plot](shap_dotplot.png)
   This plot presents a detailed view of SHAP values. Each dot stands for a dataset sample. Its color signifies the feature's value (high or low), while its x-axis placement indicates its influence on the model prediction.

   Key Takeaways:
   - **Outlet_Establishment_Year** and **Item_MRP** emerge as the most influential features, impacting predictions by ~293.2 and ~256.96, respectively.
   - **Item_Weight** and **Item_Visibility** also exert a substantial influence.
   - Many Item_Identifier values, among others, exert a negligible influence.

### Local Interpretability with SHAP and LIME

Local explanations zoom in on specific instances, shedding light on the model's behavior concerning those points:

1. **SHAP Force Plots**: Force plots for instances with both low and high sales depict the contribution of each feature to that particular prediction.

2. **LIME Explanations**: LIME provides an alternative method for local interpretability, targeting individual predictions and using locally fit surrogates for explanations.

   Key Observations:
   - For the instance with the lowest sales (index: 6950), certain features significantly drove down the sales prediction.
   - For the instance with the highest sales (index: 1450), a different set of features influenced the prediction.

### Conclusion

Model interpretability is of paramount importance, particularly in business contexts like sales predictions. Tools such as SHAP and LIME demystify complex models, offering both global and local explanations. Businesses can harness these insights to refine their strategies and make more data-driven decisions.

## How to Use

1. **Clone the Repository:** Start by cloning this repository to your local machine.
2. **Install Necessary Libraries:** Ensure you have all required Python libraries installed. They can be found at the beginning of the notebook.
3. **Run the Notebook:** Open the provided notebook for an in-depth, step-by-step walkthrough of every stage of this project, from data preprocessing to model interpretation.
4. **View Visuals:** Navigate to the "Project 1[Revisited]" folder to see the visual interpretations of model predictions.

Enjoy exploring the intricacies of sales prediction interpretation!


