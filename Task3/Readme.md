# House Price Prediction - Linear Regression

This is Task 3 of my AI and ML Internship. In this task I built a Linear Regression 
model to predict house prices based on features like area, bedrooms, bathrooms etc.

## Dataset

- Name: House Price Prediction Dataset
- File: Housing.csv
- Source: Kaggle

## What I Did

1. Loaded the dataset and checked for missing values.
2. Converted yes/no columns into 1/0 using map function.
3. Encoded furnishingstatus column using Label Encoding.
4. Split the data into 80% training and 20% testing.
5. Trained a Linear Regression model using sklearn.
6. Predicted house prices on test data.
7. Evaluated the model using MAE, MSE and R2 score.
8. Plotted Actual vs Predicted price graph.
9. Checked feature coefficients to see which features affect price the most.

## Results

- MAE tells how much the prediction was off on average.
- R2 score close to 1 means the model is performing well.
- Area and bathrooms had the highest positive impact on price.

## Files

- housing-price-prediction.py — main code
- Housing.csv — dataset
- README.md — this file

## Libraries Used

Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
