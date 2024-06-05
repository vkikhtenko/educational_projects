# Description of the project

You are a Data Sciense specialist at a carsharing company. You have received an order: you need to create a system that could assess the risk of an accident along the selected route. Risk refers to the probability of an accident with any damage to the vehicle. As soon as the driver has booked a car, got behind the wheel and chosen a route, the system should assess the level of risk. If the risk level is high, the driver will see a warning and recommendations along the route.
The idea of creating such a system is under preliminary discussion and elaboration. There is no clear algorithm of operation and similar solutions on the market yet. The current task is to understand whether it is possible to predict an accident based on historical data from one of the regions.

The idea of solving the problem from the customer: 

* Create an accident prediction model (the target value is at_fault (culprit) in the parties table)
    * For the model, select the type of culprit — car only.
    * Select cases where an accident has caused any damage to the vehicle, except for the SCRATCH type.
    * For modeling, limit yourself to data for 2012 — they are the most recent.
    * A prerequisite is to take into account the age factor of the car.
    
* Based on the model, to investigate the main factors of an accident.

* To understand whether the results of modeling and analysis of the importance of factors will help answer the questions:
    * Is it possible to create an adequate driver risk assessment system when issuing a car?
    * What other factors should be considered?
    * Do I need to equip the car with any sensors or camera?

The customer suggests that you work with the incident database and form your own ideas for creating such a system.

#  The general conclusion of the model

* As a result of this project, 4 models were created: logistic regression, decision tree, random forest and catboost. Catboost performed best in all three metrics (precision, recall, roc-auc)

* As for me, the model turned out to be insufficiently accurate. I can assume that this happened for the following reasons

    * could have misunderstood the task
    * I think it would be possible to try to take data for a longer period, and not just limit it to 2012
    * many features have been abandoned due to the fact that they appear after an accident
    
* It is likely that additional factors such as the number of accidents involving the driver, the number of intersections on the way, and the length of the created route could be used to improve the model

* One of the significant parameters is the presence/absence of a control system. If you install control devices, this can reduce the risk of an accident for drivers (judging by the analysis above)
    
* You can consider an option with built-in breathalyzers with the need for periodic checks to reduce accidents with drivers under the influence of alcohol
