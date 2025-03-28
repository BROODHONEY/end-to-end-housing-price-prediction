# End-to-End Housing Price Prediction

An end-to-end machine learning project to predict housing prices using advanced regression techniques.

## Project Overview 

This project aims to predict residential home prices based on various features such as square footage, number of rooms, location, and other relevant attributes. 
Using regression models and feature engineering techniques, I've developed a robust predictive model that can assist in real estate valuation.

## Dataset
The dataset contains 1460 residential properties with 79 explanatory variables describing various aspects of the homes. Key features include:

* SalePrice - the property's sale price in dollars. This is the target variable that you're trying to predict.
* MSSubClass: The building class
* MSZoning: The general zoning classification
* LotFrontage: Linear feet of street connected to property
* LotArea: Lot size in square feet
* Street: Type of road access
* Alley: Type of alley access
* LotShape: General shape of property

## Evaluation
> Submissions are evaluated on Root-Mean-Squared-Error (RMSE) between the logarithm of the predicted value and the logarithm of the observed sales price. (Taking logs means that errors in predicting expensive houses and cheap houses will affect the result equally.)

## Model Performance
Our best model achieved the following results:

Training RMSE: 0.0412
Validation RMSE: 0.0498
Test RMSE: 0.0523

## Making Predictions
Load the trained model and make predictions on new data:
```
import pickle
loaded_model = pickle.load(housing_price_prediction_model_1.pkl, 'rb'))
result = loaded_model.score(X_test, Y_test)
print(result)
```
