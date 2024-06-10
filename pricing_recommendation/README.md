## Exploratory data analysis. Research of apartment sale ads:

You have at your disposal the data of the real estate sales service — an archive of ads for the sale of apartments in St. Petersburg and neighboring settlements for several years. You need to learn how to determine the market value of real estate. To do this, conduct a exploratory analysis of the data and set the parameters that affect the price of the objects. This will allow you to build an automated system: it will track down anomalies and fraudulent activity.

## Used libraries:

matplotlib, numpy, pandas, plotly, seaborn, sklearn, tqdm

## Conclusion:

I uploaded the data and evaluated the available information using the .info() and .describe() methods. I built histograms to estimate the distribution of data. I evaluated the correlation between the predictors and then decided to delete the number of calls due to the high correlation with the number of minutes.

I divided the data into 3 samples: training, validation, and test in the proportions of 60/20/20.

I started by learning the decision tree. I created a loop in which I changed the classification criteria and the depth of the tree. As a result, the maximum accuracy was obtained on a model with a depth of 3 and the gini classification criterion. I have built a training schedule for the model. I saw from it that there was no particular difference between the classification criteria. I also visually determined that after a tree depth of 2-3, accuracy differs greatly in the training and validation samples. As I understand it, this is a sign that the model with greater depth has been retrained.

Next, I trained a random forest model. This time I created two cycles in which, along with the depth of the tree, I also changed the number of evaluators. As a result, the model showed the maximum accuracy and the number of evaluators 34 and the depth of the tree 12. I have plotted learning curves depending on the number of evaluators and the depth of the tree. The graphs show that as the maximum depth of the tree increases, the difference between accuracy in the training sample and in the validation sample increases.

Next, I tried to build a model of logistic regression. But it showed a worse result than the previous two models. I tried to fix this by standardizing the predictor data. This improved the result from 0.71 to 0.75, but the result still remains lower.

I tested the decision tree and random forest models on test data. The results were comparable. After that, I checked the accuracy of the dummy classification prediction. As a result, the accuracy of all our models was higher. We can say that the models have been tested for correctness.
