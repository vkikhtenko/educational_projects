# A project for Wikishop
Trained the model to classify comments into positive and negative ones

# Used libraries
optuna, nltk, re, catboost, pandas, matplotlib, numpy, scipy, sklearn, worldcloud

# Conclusions

* Saved, cleaned and lemmatized the data
* Implemented text vectorization using TF-IDF
* Tested three models: logistic regression, decision tree and catboost
* The catboost model turned out to be the best
* Checking the catboost model showed that the metric on the test sample meets the requirements of the project, i.e. it turned out to be at least 0.75

* Also tried to use bert to vectorize text. I had to abandon this idea due to the rather long and costly conversion
