# Social Activism Attitude Prediction

This repository contains Python code for analyzing factors that predict individuals' attitudes towards social activism. The dataset used in this analysis is derived from the **7th World Values Survey Dataset**, which was cleaned using R. Additionally, the **individualism** data was compiled from other public research related to **Hofstede's Cultural Dimensions**. The machine learning tasks were carried out in a Kaggle notebook environment, leveraging GPU resources for efficient model training.

## Project Overview

In this project, the goal was to explore the potential factors that influence an individual's attitude towards social activism. After preparing the dataset, I applied machine learning techniques to build a predictive model. Specifically, I focused on:

1. **Data Preprocessing and Cleaning**: Data was first cleaned and processed using R to ensure it's in an optimal format for modeling. Missing values were imputed using the **`missRanger`** R package, a fast random forest algorithm that efficiently imputes missing data.
2. **Model Selection and Training**: The primary models used for prediction were **LASSO** and **Ridge Regression**, with **XGBoost** as the main model. The linear models (LASSO and Ridge) were used for benchmarking.
3. **Hyperparameter Optimization**: Hyperparameters were tuned using the **Optuna** optimization library to achieve better model performance.
4. **Feature Importance Analysis**: After training the model, I employed **DALEX** to visualize feature importance and identify which factors contribute most to the prediction.

### Key Insights:
The results suggest that **individualism** is the most important factor in predicting an individual's attitude towards social activism.

## Data Details

- **Dataset Size**: 82,061 rows and 244 columns in the **7th World Values Survey Dataset**.
- **Individualism Data**: Additional data on **individualism** was compiled from other public research on **Hofstede's Cultural Dimensions**, providing valuable cultural context for the analysis.
- **Missing Data**: Missing values in the **World Values Survey Dataset** were imputed using the **`missRanger`** R package, which applies a random forest-based approach for imputing missing data efficiently.

## Requirements

Before running the code, ensure you have the following dependencies installed:

- Python 3.x
- Libraries:
  - pandas
  - numpy
  - scikit-learn
  - xgboost
  - optuna
  - dalex
  - matplotlib
  - seaborn
  - pyreadr

You can install the required packages via `pip`:

```bash
pip install pandas numpy scikit-learn xgboost optuna dalex matplotlib seaborn pyreadr
