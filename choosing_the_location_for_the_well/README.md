## Choosing the location for the wellsite
Let's say you work for a mining company. We need to decide where to drill a new well.

You have been provided with oil samples in three regions: in each 10,000 fields, where the quality of oil and the volume of its reserves were measured. Build a machine learning model that will help determine the region where mining will bring the greatest profit. Analyze the possible profits and risks with the Bootstrap technique.

#### Steps to select a location:

They are looking for deposits in the selected region, and the values of the signs are determined for each;
Build a model and estimate the volume of stocks;
Deposits with the highest value estimates are selected. The number of deposits depends on the company's budget and the cost of developing one well;
The profit is equal to the total profit of the selected fields.


## Conclusions on the project


1. Started the project by uploading data for all three regions and analyzing the data:

1.1. Using the info() method, I determined that there are no gaps in the data. I decided to check the correlations between the data. I looked at Pearson correlations to determine dependencies. I built histograms for each feature. The distribution of the same criteria is different for different regions.

1.2. Set the well id as the index.

1.3. Divided the samples into features and target.

1.4. Divided the samples into training and test samples in the proportions of 75/25.

1.5. Standardized feature data for all three regions.


2. Training and testing of models.

2.1. I trained three linear regression models for each region and derived three metrics for each of them: RMSE, MAE, R squared.

2.2. In total, some regions have the best metrics.


3. Preparation for profit calculation

3.1. Retained the cost of 1000 m3 of product and development costs as constants for calculation.

3.2. Calculated the required number of deposits for each region for the payback of development, depending on the average volume of reserves for each well in the region. As a result, it turned out that it is impossible for any region to achieve the necessary benefits from the development of 200 wells. The third region with 234 required wells turned out to be the closest.


4. Calculation of profit and risks

4.1. Set a function for calculating the potential profit from two hundred wells

4.2. Applied bootstrap for each region. At the same time, 500 wells were randomly selected 1000 times, from which 200 of the most voluminous were selected for development. Using the function created earlier, the profit is calculated for each iteration.

4.3. To estimate the confidence interval, I used the following formula: (mean +- t-value * RMSE * cost of thousand cubic meters of product)

4.3* Corrected this point. Now the confidence interval is considered simpler. Just by quantiles. I also calculated the percentage of negative profit.

4.4. In total, it was decided to choose a second region for well development with a 95% confidence interval of profit from 68.87 to 931.55 million rubles. And the percentage of negative profit is 1%.
