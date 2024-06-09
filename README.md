

<center><h1>Yandex.Praktikum Data Science Plus Projects</h1></center>

<p align=center>
Repository containing portfolio of data science projects completed during the training courses at <a href="https://praktikum.yandex.ru/">Yandex.Praktikum</a><br>
Presented in the form of iPython Notebooks and readme markdown files. <br>

<br>
  <a href="https://github.com/vkikhtenko/educational_projects/blob/master/yandex_ds_plus_certificate_en.pdf"><b>Certificate of completion the course (English version)</b> :mortar_board: </a><br>
    <a href="https://github.com/vkikhtenko/educational_projects/blob/master/yandex_ds_plus_certificate_ru.pdf"><b>Certificate of completion the course (Russian version)</b> :mortar_board: </a>
</p><br>

<table width=100% valign=top >
  <tr>
    <td width=25%>Project</td>
    <td>Description</td>
    <td width=20%>Used libraries</td>
  </tr>
        <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/a_project_for_wikishop">A project for Wikishop</a></td>
    <td>An online store launches a new service. Now users can edit and add product descriptions, just like in wiki communities. That is, clients offer their edits and comment on the changes of others. The store needs a tool that will search for toxic comments and send them for moderation.</td>
    <td>optuna, nltk, re, catboost, pandas, matplotlib, numpy, scipy, sklearn, worldcloud</td>
  </tr>
      <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/california_real_estate">California real estate</a></td>
    <td>In the project, you need to train a linear regression model based on housing data in California in 1990. Based on the data, it is necessary to predict the median cost of a house in a residential area. Train the model and make predictions on the test sample. To assess the quality of the model, use the RMSE, MAE and R2 metrics.</td>
    <td>numpy, pandas, phik, plotly, pyspark, seaborn, matplotlib</td>
  </tr>
    <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/car_accidents">Car accidents</a></td>
    <td>You are a Data Sciense specialist at a carsharing company. You have received an order: you need to create a system that could assess the risk of an accident along the selected route. Risk refers to the probability of an accident with any damage to the vehicle. As soon as the driver has booked a car, got behind the wheel and chosen a route, the system should assess the level of risk. If the risk level is high, the driver will see a warning and recommendations along the route.
The idea of creating such a system is under preliminary discussion and elaboration. There is no clear algorithm of operation and similar solutions on the market yet. The current task is to understand whether it is possible to predict an accident based on historical data from one of the regions.</td>
    <td>matplotlib, numpy, pandas, phik, sqlalchemy, sklearn</td>
  </tr>
  <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/choosing_the_location_for_the_well">Choosing the location for the well</a></td>
    <td>Let's say you work for a mining company. We need to decide where to drill a new well.
You have been provided with oil samples in three regions: in each 10,000 fields, where the quality of oil and the volume of its reserves were measured. Build a machine learning model that will help determine the region where mining will bring the greatest profit. Analyze the possible profits and risks with the Bootstrap technique.</td>
    <td>matplotlib, numpy, pandas, plotly, scipy, seaborn, sklearn, ydata_profiling</td>
  </tr>
  <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/customer_outflow">Customer outflow</a></td>
    <td>Customers began to leave the bank. Every month. A little, but noticeable. Bank marketers have found that it is cheaper to retain current customers than to attract new ones.
It is necessary to predict whether the client will leave the bank in the near future or not. You are presented with historical data on customer behavior and termination of contracts with the bank.
Build a model with an extremely high value of F1-measures. To pass the project successfully, you need to bring the metric to 0.59. Check the F1 measure on the test sample yourself.
Additionally, measure AUC-ROC, compare its value with the F1 measure.</td>
    <td>matplotlib, numpy, pandas, phik,  plotly, seaborn, sklearn, tqdm</td>
  </tr>
  <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/determining_the_cost_of_cars">Predicting the cost of cars</a></td>
    <td>The car sales service is developing an application to attract new customers. It allows you to quickly find out the market value of your car. Historical data is at your disposal: technical specifications, complete sets and prices of cars. You need to build a model to determine the cost. 
Important to the customer:
- prediction quality;
- prediction speed;
- training time.</td>
    <td>lightgbm, matplotlib, numpy, pandas, phik,  plotly, seaborn, sklearn</td>
  </tr>
  <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/research_of_apartment_sale_ads">Research of apartment sale ads</a></td>
    <td>You have at your disposal the data of the real estate sales service — an archive of ads for the sale of apartments in St. Petersburg and neighboring settlements for several years. You need to learn how to determine the market value of real estate. To do this, conduct a exploratory analysis of the data and set the parameters that affect the price of the objects. This will allow you to build an automated system: it will track down anomalies and fraudulent activity.
Two types of data are available for each apartment for sale. The first ones are entered by the user, the second ones are obtained automatically based on cartographic data. For example, the distance to the center, airport and other facilities — this data is automatically obtained from geoservices. The number of parks and reservoirs is also filled in without the user's participation.</td>
    <td>matplotlib, numpy, pandas, sklearn</td>
  </tr>
  <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/forecasting_taxi_orders">Forecasting taxi orders</a></td>
    <td>The taxi company has collected historical data on taxi orders at airports. To attract more drivers during peak periods, you need to predict the number of taxi orders for the next hour. Build a model for such a prediction.
The value of the RMSE metric in the test sample should be no more than 48.</td>
    <td>catboost, matplotlib, numpy, pandas, sklearn, statistics, statmodels</td>
  </tr>
  <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/forecasting_the_outflow_of_customers_in_the_hotel_chain">Forecasting the outflow of customers in the hotel chain</a></td>
    <td>The client of this research is a hotel chain.
To attract customers, this hotel chain has added to its website the ability to book a room without prepayment. However, if the customer cancelled the reservation, the company suffered losses. The hotel staff could, for example, buy groceries for the arrival of a guest or simply not have time to find another customer.
To solve this problem, you need to develop a system that predicts the cancellation of the reservation. If the model shows that the reservation will be cancelled, the client is invited to make a deposit. The deposit amount is 80% of the room rate for one day and the cost of a one—time cleaning. The money will be debited from the customer's account if they cancel the reservation anyway.</td>
    <td>matplotlib, numpy, pandas, phik, seaborn, shap, sklearn, statistics, statmodels, tqdm</td>
  </tr>
  <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/movies_research">Movies research</a></td>
    <td>You need to study the Russian film distribution market and identify current trends. Pay attention to the films that have received government support. Try to answer the question of how interesting such films are to the viewer.</td>
    <td>matplotlib, numpy, pandas, plotly, seaborn, sklearn, tqdm</td>
  </tr>
  <tr>
    <td><a href="https://github.com/vkikhtenko/educational_projects/tree/master/pricing_recommendation">Pricing recommendations</a></td>
    <td>You have at your disposal data on the behavior of customers who have already switched to these tariffs. You need to build a model for the classification task that will select the appropriate tariff. You won't need to preprocess the data - you've already done it.
Build a model with the highest accuracy value possible. To pass the project successfully, you need to bring the proportion of correct answers to at least 0.75. Check the accuracy on the test sample yourself.</td>
    <td>matplotlib, numpy, pandas, plotly, seaborn, sklearn, tqdm</td>
  </tr>
  <tr>
</table>
