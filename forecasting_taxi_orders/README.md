##  Forecasting taxi orders:

The taxi company has collected historical data on taxi orders at airports. To attract more drivers during peak periods, you need to predict the number of taxi orders for the next hour.

## Used libraries:

catboost, matplotlib, numpy, pandas, sklearn, statistics, statmodels

## Conclusions:

* Imported the necessary libraries
* Uploaded the data, resampled it by the hour
* Conducted an analysis, during which he found seasonality by day and week
* Added an offset for 24 hours and a week as features
* Allocated 10 % of the data for the test
* Trained a linear regression model
* Conducted a grid search of the catboost model
* Trained the catboost model on the best parameters from gridsearch
* The analysis of the models in the test sample showed that the linear regression model turned out to be slightly better
