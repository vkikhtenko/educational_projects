## Description of the project

You are a Data Sciense specialist at a carsharing company. You have received an order: you need to create a system that could assess the risk of an accident along the selected route. Risk refers to the probability of an accident with any damage to the vehicle. As soon as the driver has booked a car, got behind the wheel and chosen a route, the system should assess the level of risk. If the risk level is high, the driver will see a warning and recommendations along the route.

## Used libraries:

matplotlib, numpy, pandas, phik, sqlalchemy, sklearn

## The general conclusion of the model:

* As a result of this project, 4 models were created: logistic regression, decision tree, random forest and catboost. Catboost performed best in all three metrics (precision, recall, roc-auc)

* As for me, the model turned out to be insufficiently accurate. I can assume that this happened for the following reasons

    * could have misunderstood the task
    * I think it would be possible to try to take data for a longer period, and not just limit it to 2012
    * many features have been abandoned due to the fact that they appear after an accident
    
* It is likely that additional factors such as the number of accidents involving the driver, the number of intersections on the way, and the length of the created route could be used to improve the model

* One of the significant parameters is the presence/absence of a control system. If you install control devices, this can reduce the risk of an accident for drivers (judging by the analysis above)
    
* You can consider an option with built-in breathalyzers with the need for periodic checks to reduce accidents with drivers under the influence of alcohol
