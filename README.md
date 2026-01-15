# Healthy Life Expectancy (HALE) Analysis and Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-ML-F7931E)
![Status](https://img.shields.io/badge/Project-Complete-brightgreen)
![License: MIT](https://img.shields.io/badge/License-MIT-green)

This repository provides the **dataset and full reproducible workflow** used in the IEEE paper:

**Pranjal T S et al.**  
*Healthy Life Expectancy (HALE) Analysis and Prediction using Machine Learning* (IEEE, 2024)  
Paper: https://ieeexplore.ieee.org/document/10987496

# Overview

This project analyzes and predicts Healthy Life Expectancy at age 60 using machine learning models trained on World Health Organization (WHO) health and socio-economic data from 185 countries (2000–2019).
By combining robust data imputation, normalization, and model comparison, the study demonstrates the effectiveness of ensemble methods in capturing key determinants of healthy aging across populations.

# Data

The dataset is obtained from publicly available World Health Organization (WHO) global health records. It includes Healthy Life Expectancy at age 60 as the target variable along with multiple health, demographic, and socio-economic indicators.

The data covers 185 countries from 2000 to 2019, where each entry represents a country-year observation. This allows comparison across countries as well as analysis of trends over time.

# Methodology

The project follows a structured machine learning pipeline implemented using multiple Jupyter notebooks:

- **Data Preprocessing (`data_preprocessing.ipynb`)**  
  - Load the raw WHO dataset  
  - Handle missing values and clean inconsistencies  
  - Prepare the dataset for analysis  

- **Exploratory Data Analysis (`EDA.ipynb`)**  
  - Analyze HALE trends across countries and years  
  - Study data distributions and temporal patterns  
  - Visualize relationships between key indicators  

- **Feature Engineering and Normalization (`feature_engineering_and_normalization.ipynb`)**  
  - Select relevant features for modeling  
  - Normalize numerical variables to a common scale  

- **Normalized Dataset Export (`normalized_dataset_export.ipynb`)**  
  - Save the finalized normalized dataset  
  - Ensure consistent data usage across experiments  

- **Model Training and Evaluation (`model_training_and_evaluation.ipynb`)**  
  - Train multiple machine learning models to predict HALE at age 60  
  - Evaluate performance using regression metrics  
  - Compare models to identify the best-performing approach
 
# Models Used

The following machine learning models are evaluated to predict Healthy Life Expectancy at age 60 (HALE@60):

- **Linear Regression**  
  Used as a baseline model to capture linear relationships between HALE and socio-economic indicators.

- **Ridge Regression (L2 Regularization)**  
  Extends linear regression by reducing multicollinearity and overfitting through coefficient regularization.

- **Lasso Regression (L1 Regularization)**  
  Performs feature selection by shrinking less important feature coefficients to zero.

- **Random Forest Regressor (Baseline and Tuned)**  
  An ensemble model using multiple decision trees to capture complex, non-linear relationships.

- **Gradient Boosting Regressor (Baseline and Tuned)**  
  Sequential ensemble model that improves predictions by correcting errors from previous trees.

- **AdaBoost Regressor**  
  Adaptive boosting model that focuses on hard-to-predict instances using weak learners.

- **Support Vector Regressor (SVR)**  
  Regression model that fits data within a defined margin and handles moderately non-linear relationships.

These models are compared using standard regression metrics to identify the most effective approach for predicting HALE@60.

# Evaluation Metrics

Model performance is evaluated using:

- Root Mean Squared Error (RMSE)  
- Mean Absolute Error (MAE)  
- R-squared (R²)  
- Cross-validation RMSE

# Results

The results show that ensemble-based models significantly outperform linear models in predicting Healthy Life Expectancy at age 60.

Random Forest and Gradient Boosting achieve the best performance, with test R² values above 0.99 and the lowest RMSE scores. These models effectively capture non-linear relationships and complex interactions among socio-economic and health indicators.

Linear and regularized regression models perform moderately well but are limited by their linear assumptions. Support Vector Regression and AdaBoost achieve mid-range performance but do not match the accuracy of the tree-based ensemble models.


