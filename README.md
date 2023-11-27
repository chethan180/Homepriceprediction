# Housing Prices Prediction Project

This project involved building a model to predict housing prices based on economic and demographic features.

## Datasets

The following datasets were used:

- Housing unit sales
- Consumer sentiment index 
- Producer Price Index (PPI) for materials/components for construction 
- 30-year fixed mortgage rates
- PPI for transportation services
- New privately owned housing units completed
- Working age population
- Unemployment rate  
- Population growth rate
- GDP
- S&P Case-Shiller home price index (target variable)

These datasets were preprocessed by filling in missing values and merged into a single dataframe for modeling. Additional engineered features were created including lags and rolling means of the target variable. 

## Exploratory Data Analysis

- Dataset info and summary statistics were computed
- A correlation matrix heatmap was generated to understand relationships between features
- Outliers were detected and capped using the IQR method

## Modeling

An XGBoost regression model was trained to predict the Case-Shiller home price index.

The data was split 80/20 into train and test sets and standardized using MinMaxScaler.

Hyperparameter tuning was performed using GridSearchCV to select optimal parameters:

- n_estimators = 150
- max_depth = 5
- learning_rate = 0.1

The performance metrics for the final model were:

- R-squared = 0.9977628388900563 
- RMSE = 3.221665602627993

## Explainability

Partial dependence plots were generated for each feature to understand how the features impact the predicted home prices.

## Next Steps

Future work could involve:

- Incorporating additional datasets 
- Experimenting with deep learning models
