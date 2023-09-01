# ML-Bike-Sharing-Demand-Prediction---Regression
### Supervised Machine Learning 

## Business Objective
Currently rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

## Dataset Overview
- Dataset contains 8760 rows and 14 columns.
- There are no duplicate values.
- There are no null values.
- Some of the columns are Date, Rented Bike Count, Hour, Temperature, Humidity, Wind Speed, etc.

## Data PreProcessing
- On a non-functioning day we see that there are no rented bikes, so we remove the rows where Functioning Day = No. Now since we are left only one value for the column Functioning Day, we drop this column.
- Split the Date Column into 3 - Day, Month and Year. Based on the Day, created a new column if the day is Weekend or not.
- Changed the type of Hour since will be encoding the variable at a later stage.
- Renamed some column names for better readability.

## Exploratory Data Analysis
- On a weekday, between 7 AM to 9 AM and 5 PM to 7 PM the demand for bikes are high when compared to weekends.
- Demand is high during the months of April, May, June, July, August, Septmeber which comprises of Summer and Autumn season.
- The demand for bikes in Winter season is very low.
- When the Wind Speed is greater than 6.9, the demand for bikes is highest.
- When Humidity is below 20, the demand for bikes is highest.

## Feature Engineering
- Used Yeo-Johnson Transformation for making the features normally distributed and also to remove the outliers.
- Created a new feature called CalcTemperature which is combination of Temperature and Dew Point. And these two features are removed from the dataset.
- Used OneHotEncoding for categorical variables.
- Used StandardScaler for Feature Scaling.

## ML Model Implementation
- Linear Regression
- Ridge Regression
- Lasso Regression
- ElasticNet
- XGBoost

## Evaluation Metric Selection
I have considered R-squared evaluation metric for this problem. R-square represents the proportion of variance in the model. It is a relative metric which is used to compare with other models trained on the same data. It gives us a rough feel of how well our model is performing.
A model that explains no variance would have an R-square value of 0. A model with R-square value of 1 would explain all of the variance. Higher scores are better. It is also possible for R-square to be negative. Negative scores occur when the predictions that the model makes fit that data worse than the mean of the output values.

## Summary
XGBoost gives a very good R2 Score which is essential to our project. The project was successfully deployed thus enabling the business to approximate the forecast for demand of rental bikes.
