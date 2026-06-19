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

## Workflow

The project follows a complete machine learning workflow:

1. **Data Understanding**
   - Loaded training and test datasets.
   - Checked dataset shapes, column types, and target variable.
   - Analyzed the distribution of `SalePrice`.
   - Applied log transformation to reduce target skewness.

2. **Exploratory Data Analysis**
   - Investigated numerical and categorical features.
   - Analyzed correlations with `SalePrice`.
   - Identified important predictors such as `OverallQual`, `GrLivArea`, `GarageCars`, and `TotalBsmtSF`.
   - Detected potential outliers.

3. **Missing Value Handling**
   - Filled missing values based on feature meaning.
   - Treated missing values in pool, garage, basement, fireplace, alley, and fence-related features as absence of the feature.
   - Filled numerical missing values using `0`, median, or neighborhood-based median where appropriate.

4. **Feature Engineering**
   - Created new features such as `TotalSF`, `TotalBathrooms`, `HouseAge`, `RemodAge`, and `GarageAge`.
   - Added binary indicator features such as `HasGarage`, `HasBasement`, `HasFireplace`, `HasPool`, and `HasPorch`.
   - Checked and corrected inconsistent date-based values.

5. **Preprocessing**
   - Removed the `Id` column from model features.
   - Removed selected outliers from the training data.
   - Encoded categorical variables using one-hot encoding.
   - Applied scaling for linear models.

6. **Modeling**
   - Trained and compared multiple regression models:
     - Linear Regression
     - Ridge Regression
     - Lasso Regression
     - Random Forest Regressor
     - Gradient Boosting Regressor

7. **Evaluation**
   - Evaluated models using RMSE on the log-transformed target variable.
   - Used 5-fold cross-validation for more reliable performance comparison.

8. **Final Model Selection**
   - Selected `GradientBoostingRegressor` as the final model based on cross-validation results.
   - Generated prediction outputs for the test dataset.
   - Exported model comparison results and feature importance results.

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



