# Prediction of Grocery Sales

This project aims to predict grocery sales using machine learning techniques. It involves data preprocessing, model training, and local explanations using SHAP and LIME.

## Table of Contents

- [Project Overview](#project-overview)
- [Installation](#installation)
- [Data](#data)
- [Data Preprocessing](#data-preprocessing)
- [Model Training](#model-training)
- [Local Explanations](#local-explanations)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project focuses on predicting grocery sales using a RandomForestRegressor model. It includes data preprocessing, model training, and local explanation techniques.
# Prediction of Grocery Sales

This repository contains a project focused on predicting grocery sales using machine learning techniques. The project involves data preprocessing, model training, and model interpretation using SHAP and LIME.


## Example Images

Here are the explanation plots generated using LIME and SHAP for high and low sales examples:

### High Sales LIME Explanation
![High Sales LIME Explanation](/Project%201%5BRevisited%5D/high_sales_lime_explanation.png)

### High Sales SHAP Force Plot
![High Sales SHAP Force Plot](/Project%201%5BRevisited%5D/high_sales_shap_force_plot.png)

### Low Sales LIME Explanation
![Low Sales LIME Explanation](/Project%201%5BRevisited%5D/low_sales_lime_explanation.png)

### Low Sales SHAP Force Plot
![Low Sales SHAP Force Plot](/Project%201%5BRevisited%5D/low_sales_shap_force_plot.png)

## Installation

1. Clone the repository:
git clone https://github.com/yourusername/Prediction-of-Grocery-Sales.git
cd Prediction-of-Grocery-Sales


2. Install the required Python packages:
pip install -r requirements.txt


## Data

The project utilizes the "sales_predictions.csv" dataset containing various features related to grocery items and their sales.

## Data Preprocessing

The data preprocessing steps involve handling missing values, feature scaling, and one-hot encoding for categorical variables.

## Model Training

A RandomForestRegressor model is trained to predict grocery sales based on the preprocessed features.

## Local Explanations

The project employs SHAP and LIME for local explanations of model predictions. SHAP force plots and LIME explanations are generated for representative examples.

## Results

The generated SHAP force plots and LIME explanations provide insights into how specific features contribute to the model's predictions.

## Contributing

Contributions to this project are welcome! Feel free to open issues or submit pull requests.

## License

This project is licensed under the [MIT License](LICENSE).




