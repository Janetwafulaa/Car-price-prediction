# Car-price-prediction
# Car Price Prediction using Regression Models

This project applies different **regression techniques** to predict the selling price of cars based on their features.  
The goal is to compare the performance of various models and understand how regularization and non-linear transformations affect predictions.

## 📊 Models Implemented
- **Linear Regression** – Baseline model without regularization.  
- **Lasso Regression (L1 Regularization)** – Performs feature selection by shrinking some coefficients to zero.  
- **Ridge Regression (L2 Regularization)** – Handles multicollinearity by shrinking coefficients without eliminating features.  
- **Polynomial Regression** – Captures non-linear relationships by adding polynomial and interaction terms.

## ⚙️ Features
- Data preprocessing (handling missing values, outlier removal, feature scaling).  
- Train/test split for fair evaluation.  
- Model comparison using **R² Score** and **Mean Squared Error (MSE)**.  
- Cross-validation with `GridSearchCV`, `RidgeCV`, and `LassoCV` to find the best hyperparameters.  
- Visualization of predicted vs actual prices.  

## 🛠️ Technologies Used
- Python  
- Pandas, NumPy – data manipulation  
- Scikit-learn – machine learning models  
- Matplotlib – visualizations  
