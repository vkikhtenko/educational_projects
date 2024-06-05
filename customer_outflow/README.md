Customer outflow
Customers began to leave the bank. Every month. A little, but noticeable. Bank marketers have found that it is cheaper to retain current customers than to attract new ones.

It is necessary to predict whether the client will leave the bank in the near future or not. You are presented with historical data on customer behavior and termination of contracts with the bank.

Build a model with an extremely high value of F1-measures. To pass the project successfully, you need to bring the metric to 0.59. Check the F1 measure on the test sample yourself.

Additionally, measure AUC-ROC, compare its value with the F1 measure.

Data source: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

Features

RowNumber — an index of the row in the data

CustomerId — the unique identifier of the client

Surname

CreditScore — credit rating

Geography — country of residence

Gender

Age

Tenure — how many years has a person been a customer of the bank

Balance — account balance

NumOfProducts — the number of bank products used by the customer

HasCrCard — availability of a credit card

IsActiveMember — client activity

EstimatedSalary — estimated salary

Target

Exited — the fact of the client's leaving


Conclusions on the project
I started the project by uploading data. Saved the data to the data variable.
Then I moved on to data analysis.

2.1. Using the info() method, I determined that a part of the data is missing in the tenure column. I decided to check if there is any connection with other data in order to fill them in. To do this, I built histograms for each feature. I looked at Pearson correlations and used phik_matrix to determine dependencies. As a result, I did not find the dependence of this variable with other data and decided to delete them. But the question remained open.: What could be done with them?

2.2. During the analysis, I noticed the following data features:

  2.2.1. Active and inactive users are approximately equal

  2.2.2. Salaries are distributed suspiciously evenly

  2.2.3. There are a lot of users with zero balance

  2.2.4. Those who refused the bank's services are approximately 20%.

  2.2.5. The vast majority of users use one or two products of the bank.

  2.2.6. The median age is around 40 years.

  2.2.7. The duration of using the bank's services is distributed evenly among users, but those who use it for less than a year or more than 10 years are eliminated
2.3. Checked the class imbalance. The ratio of remaining customers to those who have left the bank is about 80 to 20%.

2.4. Divided the samples into training, validation and test samples in the proportions of 60/20/20. I removed the columns with the last name and id from the predictors, since this information is unlikely to help us classify users correctly

2.5. Converted the data in the Geography, Gender columns into numerical variables using the OHE method. In order not to fall into the trap of fictitious signs, I passed drop_first=True.

2.6. Standardized the data in all three samples

I moved on to the study of problem

3.1. I trained models of logistic regression, decision tree and random forest. I checked the F1 and AUC-ROC metrics on each of them and built a ROC curve. As a result, it turned out that the random forest model works best on data with an imbalance. F1 = 0.626, AUC-ROC = 0.863.

3.2. To correct the imbalance, I used the downsampling technique. I trained the same models. I checked the F1 and AUC-ROC metrics on each of them and built a ROC curve. As a result, it also turned out that the random forest model works best. F1 = 0.622, AUC-ROC = 0.864. At the same time, the F1 metric of the logical regression increased from 0.330 to 0.514.

3.3. For comparison, I used the upsampling technique. I trained the same models. I checked the F1 and AUC-ROC metrics on each of them and built a ROC curve. As a result, it also turned out that the random forest model works best. F1 = 0.649, AUC-ROC = 0.870.

Testing random forest models with upsampling and downsampling.

4.1. In the test sample, a random forest model trained on data using the upsampling technique showed the following metrics: F1 = 0.648, AUC-ROC = 0.849

4.2. In the test sample, a random forest model trained on data using the downsampling technique showed the following metrics: F1 = 0.622, AUC-ROC = 0.831

4.3. In total, we choose a random forest model with upsampling due to higher metrics.

Now this model can be used to identify customers who have a high risk of abandoning the bank's services. Now we can use this information to take measures to prevent them from leaving.
