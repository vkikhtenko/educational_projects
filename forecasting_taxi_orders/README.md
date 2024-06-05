#  Forecasting taxi orders

The taxi company has collected historical data on taxi orders at airports. To attract more drivers during peak periods, you need to predict the number of taxi orders for the next hour. Build a model for such a prediction.

The value of the *RMSE* metric in the test sample should be no more than 48.

You need to:

1. Download the data and resample it one hour at a time.
2. Analyze the data.
3. Train different models with different hyperparameters. Make a test sample of 10% of the original data.
4. Check the data on the test sample and draw conclusions.


The number of orders is in the `num_orders` column.

# Conclusions:

* Imported the necessary libraries
* Uploaded the data, resampled it by the hour
* Conducted an analysis, during which he found seasonality by day and week
* Added an offset for 24 hours and a week as features
* Allocated 10 % of the data for the test
* Trained a linear regression model
* Conducted a grid search of the catboost model
* Trained the catboost model on the best parameters from gridsearch
* The analysis of the models in the test sample showed that the linear regression model turned out to be slightly better
