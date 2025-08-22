
# Car Price Prediction using Regression Models

This project applies different **regression techniques** to predict the selling price of cars based on their features.  
The goal is to compare the performance of various models and understand how regularization and non-linear transformations affect predictions.

##  Models Implemented
- **Linear Regression** – Baseline model without regularization.  
- **Lasso Regression (L1 Regularization)** – Performs feature selection by shrinking some coefficients to zero.  
- **Ridge Regression (L2 Regularization)** – Handles multicollinearity by shrinking coefficients without eliminating features.  
- **Polynomial Regression** – Captures non-linear relationships by adding polynomial and interaction terms.

##  Features
- Data preprocessing (handling missing values, outlier removal, feature scaling).  
- Train/test split for fair evaluation.  
- Model comparison using **R² Score** and **Mean Squared Error (MSE)**.  
- Cross-validation with `GridSearchCV`, `RidgeCV`, and `LassoCV` to find the best hyperparameters.  
- Visualization of predicted vs actual prices.  

## Technologies Used
- Python  
- Pandas, NumPy – data manipulation  
- Scikit-learn – machine learning models  
- Matplotlib – visualizations

  ## Explanation of the model and the Visualizations and Insights derived
**Data Cleaning Part**
  
  - Loading the dataset and displaying the first rows to see what the rows and columns look like
  - Checking for missing values in the dataset to ensure there is no missing values because we want to avoid bias and ensure models can actually run
  - Filling missing values, filling missing values can sometimes be better than dropping rows because we will be preserving the data and ensuring our model gets as much data, and preventing bias
  - Removing duplicate rows from the dataset to avoid bias in the model because some rows will appear more than others
  - Knowing all possible values in a categorical column is important before encoding because you might come across unknown categories during encoding
  - Checking outliers because they may affect model accuracy, in that they will distort parameter estimates and increase error variance
  - Checking if any numerical columns are stored as strings and converting them to numbers to ensure models accept them
  - creating necessary columns that you will need to improve model efficiency
  - resetting index after cleaning
  - saving your cleaned dataset

**Exploratory Data Analysis**

  - Diesel was the most common type of fuel used
  - Histogram of the selling prices- here we can see that most cars selling prices ranged between 0 and 2000000
  - Relationship between car age and selling price using a scatter plot- we could see that the higher the selling price, the lower the car age, and vice versa
  - Grouping cars by fuel type and finding the average selling price for each group - out of all the categories, diesel had the highest average selling price
  - Bar chart showing the number of cars per transmission type - In this bar chart manual transmission was used the most in most cars
  - Car with the highest mileage in the dataset - the car with the highest mileage was Maruti Alto 800 CNG LXI Optional
  - Correlation between mileage and selling price - 0.12 as observed in the correlation heatmap 
  - Automatic cars are more expensive than manual cars
  - A line chart showing the trend of selling prices over the years - here we can see prices increased as years went by
  - The brand that appears most in the dataset is the Maruti brand

**Machine Learning**

 - Assumptions of Linear regression(Linearity,Independence of errors (No autocorrelation),Homoscedasticity,Normality of residuals)
 - Using linear regression after training the model, I found the coefficient and intercept as Intercept: 1901561.3870947324
  Coefficients:
  mileage(km/ltr/kg): -34687.28384660838
  car_age: -62721.03253147038
 - The R² was 0.35 and MSE was 117648041930.44037
 - On Lasso regression, the metrics were R²: 0.3518437325863625,MSE: 117648042612.38016, showing it performed the same as Linear regression

