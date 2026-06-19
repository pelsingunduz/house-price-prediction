# House Price Prediction

This project predicts residential house prices using the Kaggle House Prices dataset.  
The main goal of the project is to practice and demonstrate a complete machine learning workflow, including data understanding, exploratory data analysis, missing value handling, feature engineering, model comparison, cross-validation, and model interpretation.

## Project Overview

House price prediction is a supervised machine learning regression problem.  
The target variable is `SalePrice`, which represents the final sale price of each house.

The project focuses on building a clean and understandable machine learning pipeline rather than only optimizing for a Kaggle score.

## Dataset

The dataset is based on the Kaggle House Prices - Advanced Regression Techniques competition.

Main files used:

- `train.csv`
- `test.csv`
- `data_description.txt`

The dataset contains numerical and categorical features related to house characteristics such as:

- Overall quality
- Living area
- Garage capacity
- Basement area
- Year built
- Neighborhood
- Bathrooms
- Porch area

## Project Structure

```text
house-price-prediction/
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── data_description.txt
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_eda_missing_values.ipynb
│   └── 03_preprocessing_modeling.ipynb
├── outputs/
│   ├── model_cv_results.csv
│   ├── predictions_gradient_boosting.csv
│   └── feature_importance_gradient_boosting.csv
├── src/
├── README.md
├── requirements.txt
└── .gitignore


