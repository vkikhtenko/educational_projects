# Predicting the cost of housing

In the project, you need to train a linear regression model based on housing data in California in 1990. Based on the data, it is necessary to predict the median cost of a house in a residential area.

## Used libraries:
numpy, pandas, phik, plotly, pyspark, seaborn, matplotlib

## Conclusion:
Started by installing and importing the necessary libraries

Initialized the local spark session

Read the data, checked the data type, found gaps in the total_bedrooms column

Filled in the gaps with the median value

Transformed the categorical variable via OHE

Standardized numeric variables (Most likely made a mistake here. The data has not been standardized in the way I imagined it to be)

Built two models: 

  1. with all variables,
     
  2. without categorical

The metrics turned out to be comparable, but the first model with categorical features turned out to be slightly better
