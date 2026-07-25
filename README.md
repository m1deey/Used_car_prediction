Used Car Price Prediction

Machine Learning project that predicts used car prices using several regression models. The workflow includes data cleaning, feature engineering, exploratory data analysis, model training, and model comparison.

---

Project Overview

This project uses a used-car dataset containing information such as:

- Brand
- Model
- Mileage
- Model year
- Engine specifications
- Fuel type
- Transmission
- Exterior and interior colors
- Accident history
- Price (target)

The goal is to build a model that can estimate the selling price of a car from these features.

---

Data Cleaning

Main preprocessing steps:

- Removed missing values in critical columns
- Converted mileage from strings like "45,000 mi." to integers
- Converted price from strings with "$" to numeric values
- Created a new feature model_age
- Grouped rare colors into Other
- Encoded categorical variables using One-Hot Encoding
- Removed extreme outliers in "model_age"

---

Exploratory Data Analysis

Mileage vs Price

"Mileage vs Price" (images/Scatter_actual_predicted.jpg)

The scatter plot shows that car price generally decreases as mileage increases.

---

Models Tested

Model| R² Score
Linear Regression| 0.05
Linear Regression (Log Target)| 0.74
Ridge Regression| ~0.74
Lasso Regression| ~0.74
Random Forest| 0.77
XGBoost| 0.84

---

Best Model: XGBoost

XGBoost achieved the best performance with an R² score of approximately 0.84, meaning it explains about 84% of the variance in used car prices.

---

Feature Importance

Top 10 most important features according to XGBoost:

"XGBoost Feature Importance" (images/Feature_importance.png)

Mileage and model age were the most influential features, followed by horsepower, cylinders, engine size, and some premium brands.

---

Actual vs Predicted

The following plot compares the real prices with the prices predicted by XGBoost.

"Actual vs Predicted" (images/Actual_vs_Predicted.jpg)

Most points are close to the diagonal line, which indicates that the model predicts prices accurately.

---

Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

---

Conclusion

This project demonstrates a complete machine learning workflow for a real-world regression problem. After comparing multiple models, XGBoost provided the best accuracy and produced reliable predictions for used car prices.

The project also highlights the importance of data cleaning, feature engineering, and model comparison in achieving strong machine learning performance.
