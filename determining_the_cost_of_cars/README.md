# Determining the cost of cars

The car sales service is developing an application to attract new customers. It allows you to quickly find out the market value of your car. Historical data is at your disposal: technical specifications, complete sets and prices of cars. You need to build a model to determine the cost. 

Important to the customer:

- prediction quality;
- prediction speed;
- training time.

### Features

* DateCrawled — date when the questionnaire was downloaded from the database
* VehicleType — type of car body
* RegistrationYear — the year of registration of the car
* Gearbox — type of gearbox
* Power — power (hp)
* Model — car model
* Kilometer — mileage (km)
* RegistrationMonth — month of car registration
* FuelType — fuel type
* Brand — the brand of the car
* Repaired — was the car under repair or not
* DateCreated — date of creation of the questionnaire
* NumberOfPictures — the number of photos of the car
* PostalCode — postal code of the questionnaire owner (user)
* lastSeen — the date of the user's last activity
* Target feature
* Price — price (euro)


## Conclusions

**The course of work was as follows:**
* Installed and imported the necessary libraries
  
* Read the data, saved it to the df variable
  
* Estimated the percentage of omissions in the data, built histograms for each feature
  
* Deleted zero values based on the target attribute
  
* Deleted all values from the NumberOfPictures column because all values were zero
  
* Checked the data in the RegistrationYear column. Deleted data in which the year was earlier than 1950 and later than 2016
  
* Deleted the data in the DateCrawled, DateCreated, lastSeen columns due to the fact that they are limited to the period from March to April 2016.
   
* After deleting the features with dates, I set up the phik correlation matrix. Determined that Model correlates with Brand and VehicleType
  
* Filled in the gaps with unknown values in the VehicleType, Gearbox, FuelType, Repaired, Model features
  
* Having filled in all the data with plugs, I built graphs of the spread of the target dependence on each feature
  
* I found that there are zero values in the RegistrationMonth column. Due to the fact that there were quite a lot of them, I replaced this feature with a discrete one, which indicated whether there was data on the month of registration or not
  
* Deleted the PostalCode column due to the inability to determine the exact location
  
* A lot of outliers (zeros and extremely high values) were detected in the Power column. I did not delete them, but filled them with median values for each model
  
* Deleted the Model column due to the correlation with Brand and VehicleType, as well as due to the large number of unique values, which, when encoded via OHE, would have given many new columns
  
* In the Repaired column, I replaced all previously filled in gaps with unknown values with yes
  
* Converted the column with the year of registration of the car to the "prescription" of registration of the car, i.e. in the column indicated how many years have passed from the moment of registration of the car to the moment of determining its value
  
* Checked the data again. I found a gap in the Power column, deleted it
  
* Divided the data into training and test samples
  
* Created a pipeline for converting categorical features through OHE and standardizing numeric features
  
* Trained the decision tree model using gridsearch. RMSE on the training sample it turned out 2022.2
  
* I trained a gradient boosting model using gridsearch. RMSE, it turned out to be 1746 on the training sample
  
* In the test sample, the decision tree model showed RMSE 2074, and the gradient boosting model 1773
  
* In terms of model learning time, the decision tree wins, but only by a minute
  
* In total, the gradient boosting model performed better
