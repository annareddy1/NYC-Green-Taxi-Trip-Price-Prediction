# NYC-Green-Taxi-Trip-Price-Prediction
This project provides insights into NYC Green Taxi data, uncovering travel patterns, predicting fares, and optimizing pickup locations using machine learning techniques.

This project delves into analyzing NYC Green Taxi Trip Data from January 2022 to January 2023. Green Taxis in NYC, authorized for street-hail pickups outside the central business district and airports, were introduced to extend taxi services to underserved areas beyond Manhattan. Yellow Taxis, traditionally dominant in Manhattan and airport street-hail services, now share territories with Green Taxis, expanding the latter's reach.

The project focuses on utilizing machine learning techniques for regression and classification to achieve two primary goals:

- Fare Amount Prediction: Constructing a regression model utilizing features such as pickup and drop-off locations, trip distance, DateTime, and pertinent attributes. This model
  predicts the fare amount for individual taxi trips, enhancing accuracy in fare estimation.

- Profitable Pickup Location Identification: Developing a clustering model using pickup locations, trip distances, and fare amounts to identify profitable pickup locations for green
  taxis. This analysis assists drivers in optimizing their pickup strategies for increased profitability.

### Dataset Overview:

- Trip Record Data: 908,613 trips obtained from the New York City Taxi and Limousine Commission (TLC).
- Taxi Zone Map Dataset: Used to map location IDs in the main dataset with NYC Borough, Zone, and service zone (265 records).
- Holiday Dataset: A new dataset generated to explore trip details on holidays, working days, and weekends (23 holidays).

### Key Project Steps:

1. Feature Engineering:

Taxi Zone Integration
Column Selection and Removal: Dropping unnecessary columns and those with no entries.
Column Renaming for uniformity.
Trip Filtering based on fare amount, trip distance, and time constraints.
Handling Missing Values.
DateTime Feature Extraction: Creating new features like 'dayofweek', 'pickuphour', 'drophour', etc.
Congestion Surcharge Flagging.

2. Exploratory Data Analysis:

Analysis of Vendor distribution, Rate Codes, Hourly Trip Counts, Trip Distance, Fare Amount, Trip Time, etc.
Trip Distribution by Day, Pickup, and Dropoff LocationID.
Relationship between Distance vs. Fare Amount, Pickup Hour, and Weekday.
Analysis of Tip Amount relative to Hours and Weekdays.

3. Splitting Data & Dimension Reduction:

Designating 'fare_amount' as the target variable for regression.
One-hot encoding categorical variables for machine learning.
Splitting data into training and testing sets.
Conducting dimensionality reduction on independent variables.

4. Regression Modeling:

KNN Regression: Best-performing model with low Mean Squared Error (9.91) and high R-squared (0.9233).
Random Forest Regressor, Decision Tree, Linear Regression, and Lasso Regression models also analyzed.

### Conclusion:

KNN Regression stands out as the best-performing model for fare prediction.
Linear Regression and Lasso Regression exhibit relatively lower predictive accuracy.
