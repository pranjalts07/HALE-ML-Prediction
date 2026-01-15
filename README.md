# Healthy Life Expectancy (HALE) Analysis and Prediction using Machine Learning

This repository contains the **complete codebase and dataset** used in the IEEE research paper:

> **Pranjal T S et al.**  
> *Healthy Life Expectancy (HALE) Analysis and Prediction using Machine Learning*  
> IEEE, 2024  
> https://ieeexplore.ieee.org/document/10987496

The objective of this work is to **analyze and accurately predict Healthy Life Expectancy at age 60 (HALE₆₀)** across countries using socio-economic, demographic, and health indicators from the World Health Organization (WHO).

---

## 🔍 Why Healthy Life Expectancy (HALE)?

Traditional life expectancy does not account for **years lived with illness or disability**.  
**Healthy Life Expectancy (HALE)** improves on this by estimating the number of years a person can expect to live **in good health**, making it a more meaningful indicator for:

- Public health policy
- Resource allocation
- Healthcare planning
- Socio-economic development analysis

This project leverages **machine learning models** to uncover the **key determinants of HALE** and evaluate their predictive power across countries and time.

---

## 📊 Dataset

- **Source:** World Health Organization (WHO) – Global Health Observatory (GHO)
- **Coverage:** 185 countries
- **Time Period:** 2000 – 2019
- **Observations:** ~3,700 country–year records
- **Target Variable:** Healthy Life Expectancy at age 60 (HALE₆₀)
- **Encoding:** ISO-8859-1
- **Location:** `data/raw/merge.csv`

The dataset integrates mortality, morbidity, lifestyle, and socio-economic indicators and is **legally distributable WHO public data**.

---

## 🧪 Predictor Variables

Key predictors used in the study include:

- Adult mortality rate (ages 15–60)
- Probability of dying between ages 30–70 from chronic diseases
- Alcohol consumption (15+ years)
- Mean total cholesterol
- Physical inactivity prevalence
- Obesity prevalence (BMI ≥ 30)
- Raised blood pressure prevalence (ages 30–79)
- Tuberculosis deaths (excluding HIV)

These variables were selected based on epidemiological relevance and prior literature.

---

## 🛠️ Methodology Overview

### 1. Data Cleaning & Imputation
- Two-stage **median-based imputation**:
  1. Median within the same country and year
  2. Global median fallback
- Preserves regional and temporal trends

### 2. Feature Engineering & Normalization
- Log transformation for skewed variables (e.g., TB deaths, mortality rates)
- Standardization to ensure fair feature contribution
- Encoded features prepared for machine learning models

### 3. Exploratory Data Analysis (EDA)
- Temporal HALE trends (2000–2019)
- Regional comparisons
- Correlation analysis between HALE and predictors
- Country-level comparisons (e.g., high vs low HALE nations)

### 4. Machine Learning Models
The following models were evaluated and compared:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest (baseline and tuned)
- Gradient Boosting (baseline and tuned)
- AdaBoost
- Support Vector Regression (SVR)

Model performance was assessed using **RMSE**, **R²**, and **cross-validation**.

---

## 🏆 Key Results

- **Best-performing models:**  
  - Random Forest  
  - Gradient Boosting  

- **Random Forest performance:**  
  - Test RMSE ≈ **0.55**  
  - R² ≈ **0.99**

- **Most influential predictors:**  
  - Adult Mortality Rate  
  - Physical Inactivity  

Ensemble models demonstrated superior ability to capture **non-linear relationships and feature interactions** influencing HALE.

---

## 📁 Repository Structure

