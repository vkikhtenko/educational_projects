# A project for Wikishop
An online store launches a new service. Now users can edit and add product descriptions, just like in wiki communities. That is, clients offer their edits and comment on the changes of others. The store needs a tool that will search for toxic comments and send them for moderation. 
Train the model to classify comments into positive and negative ones. You have at your disposal a data set with markup on the toxicity of edits.

# Used libraries
optuna, nltk, re, catboost, pandas, matplotlib, numpy, scipy, sklearn, worldcloud

# Conclusions

* Saved, cleaned and lemmatized the data
* Implemented text vectorization using TF-IDF
* Tested three models: logistic regression, decision tree and catboost
* The catboost model turned out to be the best
* Checking the catboost model showed that the metric on the test sample meets the requirements of the project, i.e. it turned out to be at least 0.75

* Also tried to use bert to vectorize text. I had to abandon this idea due to the rather long and costly conversion
