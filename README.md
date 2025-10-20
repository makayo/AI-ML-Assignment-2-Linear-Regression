# House Price Prediction with Simple Linear Regression

## Author: MARK YOSINAO 
Machine Learning_Linear Regression, Data Cleaning, and Feature Engineering

## Environment
- Python 3.11.3
- pandas 2.1.0
- scikit-learn 1.3.1
- seaborn 0.12.2
- matplotlib 3.8.0
- numpy 1.26.0

## Project Overview
This project applies the principles of the machine learning lifecycle to predict house sale prices using a simplified version of the King County housing dataset.
The goal is to demonstrate a complete ML workflow: data cleaning, feature engineering, model training, evaluation, and visualization — all using a simple Linear Regression model to predict a continuous target variable.

## Dataset
The dataset includes housing sales data from King County, Washington. Key columns used:
- `SalePrice`: Final sale price of the house (target variable)
- `SqFtTotLiving`: Total square footage of living space
- `YrBuilt`: Year the house was built
- `YrRenovated`: Year of last renovation (if any)

## Workflow Summary

### 1. Data Cleaning
- Verified no missing values in key columns
- Removed outliers in `SqFtTotLiving` using the IQR method to reduce skew and improve model generalization

### 2. Feature Engineering
- Created `house_age` from `YrBuilt`
- Created `was_renovated` from `YrRenovated`
- These features add predictive value by capturing age and renovation status

### 3. Visualization
- Used pairplots to explore relationships between features and sale price
- Plotted residuals to assess model bias and variance

### 4. Model Training
- Split data into training and testing sets (80/20)
- Trained a Linear Regression model using `SqFtTotLiving`, `house_age`, and `was_renovated`

### 5. Evaluation
- Mean Squared Error (MSE): 33.6 billion
- R-squared (R²): 0.427
- Scatter plot shows predicted vs actual prices
- Residuals distribution is centered and symmetric

### 6. Custom Predictions
- Ran two test cases with custom input values to demonstrate model functionality

## Results
- The model explains approximately 42.7% of the variance in sale prices
- Residuals show no major bias, with a slight right tail indicating underprediction of high-value homes
- Custom predictions behave as expected: newer, larger, renovated homes yield higher predicted prices
