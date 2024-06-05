# Forecasting the outflow of customers in the hotel chain
# Description of the project
The client of this research is a hotel chain.

To attract customers, this hotel chain has added to its website the ability to book a room without prepayment. However, if the customer cancelled the reservation, the company suffered losses. The hotel staff could, for example, buy groceries for the arrival of a guest or simply not have time to find another customer.

To solve this problem, you need to develop a system that predicts the cancellation of the reservation. If the model shows that the reservation will be cancelled, the client is invited to make a deposit. The deposit amount is 80% of the room rate for one day and the cost of a one—time cleaning. The money will be debited from the customer's account if they cancel the reservation anyway.

# Business metrics and other data
The main business metric for any hotel chain is its profit. The profit of the hotel is the difference between the cost of a room for all nights and the cost of maintenance: both during the preparation of the room and during the stay of the guest.

The hotel has several types of rooms. Depending on the type of room, the cost per night is assigned. There are also cleaning costs. If the client has rented a room for a long time, then they are cleaned every two days.

The cost of the hotel rooms:

Category A: 1,000 per night, one—time service — 400; 

Category B: per night — 800, one—time service - 350; 

Category C: per night — 600, one—time service - 350; 

Category D: per night — 550, one—time service - 150; 

Category E: 500 per night, one—time service — 150; 

Category F: per night — 450, one—time service - 150; 

Category G: 350 per night, one—time service — 150.

The hotel's pricing policy uses seasonal coefficients: in spring and autumn prices increase by 20%, in summer — by 40%. The hotel's losses in case of cancellation of the room reservation are the cost of one cleaning and one night, taking into account the seasonal coefficient.

The budget for the development of the forecasting system is 400,000. At the same time, it should be taken into account that the implementation of the model should pay off during the test period. Development costs should be less than the revenue that the system will bring to the company.

# General conclusion

### Step 1

1.1. Installed and imported the necessary libraries.

1.2. Saved the training and test dataframes to variables

### Step 2

2.1. Checked the completeness of the data. No emissions were detected.

2.2. The test sample is about 33% of all data

2.3. Built histograms and barplots for the available features

2.4. I checked the dependencies between the data using the phik library. After checking, I decided to delete several features. A high correlation of the target with the customer id was observed. There were also problems with arrival_date_year, which I later deleted from the dataframe.

### Step 3

3.1. Set the function for calculating profit. 

3.2. Calculated to arrive in the current state. I applied boostrap for a 95% confidence interval of profit. I received a range from 34.08 to 35.52 million rubles.

### Step 4

4.1. Converted the data using OHE and ordinal encoding. I removed the features that correlated most with others.

4.2. Trained decision tree models, random forest, logistic regression. The best F1 metric was shown by the decision tree model. I also tried using roc-auc as a metric, but I didn't see much difference.

4.3. Set a function for calculating profit taking into account the predicted values. 

4.4. Using boostrap, I estimated a 95% confidence interval of profit for each model. The best result came from the logistic regression model

4.5. Calculated the possible profit under the ideal scenario, in which the model would predict everything correctly. 

4.6. I took 400 thousand for the development of the model. With this in mind, I obtained the final values of the economic effect of predicting potential cancellations

4.7. In total, I propose to use the decision tree model, which will bring a profit of 2.4 million rubles. during the test period

### Step 5

5.1. I tried to describe the portrait of the customer canceling the room reservation. 
As a result, the description turned out as follows: most often, customers with a PRT passport with the number of days from the booking date to the arrival date of more than 25 days, who previously canceled the reservation, cancel the reservation. Also, if the client did not have special requests, then the probability of cancellation increases.
