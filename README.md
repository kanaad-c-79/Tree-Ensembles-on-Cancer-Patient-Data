# Tree-Ensembles-on-Cancer-Patient-Data
# Description
Implemented Important Elements of tree ensembles, such as:

1) Single Decision Trees
2) Bagging/Bootsrapping/Random Forest - Independent Learning (on Bootstrapped Datasets (i.e. different random subset of the data))
3) Boosting/AdaBoost (Adaptive Boosting) - Sequential Learning
4) Feature Importance (for model accuracy/predictive performance) Methods

# Background Context
We worked with a Dataset of Colon Cancer Patients, including fields/variables/predictors, such as: Age, Gender, Topography (of Cancer), Stage (of Cancer), Class (of Cancer), Surgery details, etc.

We encoded the categorical fields/values from this dataset into numerical ones, and then we reordered the columns/fields and converted this Dataframe into an array. We then shuffled this array. We then Divided this (shuffled) array, ‘Xy’ into two arrays: 1) ‘X’, a 2D array containing all the predictors, and 2) ‘y’, a 1D array with the response/target. We then Split both these arrays into – 50% training data, 25% validation data, 25% test data.

# Fitting a Single Decision Tree
We fit decision trees with different depths up to max_depth = 15. These different decision trees were trained on/learnt from our training data. We then saw how this (trained) decision tree performed/its accuracy on - both the training set and the validation set - for each different depth (1-15). -> We then took the best max_depth for our decision tree, which was the max_depth for which the decison tree had the best performance/accuracy on the validation set. 

# Random Forest Classifier
We defined a Random Forest Classifier, which was also trained on/learnt from our training data. With default parameters, we then saw how this (trained) RF Classifier performed/its accuracy on - both the training set and the validation set. 

(In random forest classifiers, the algorithm only considers a subset of the features at each split. This is controlled using the max_features argument. Normally this subset size is set to the square root of the total number of features.) 

However, here we played around with the max_features argument, setting it equal to both 'sqrt' (default in sklearn) and 'None'. (When max_features = None the algorithm is using all the features at every split, like a standard decision tree.) 

As suspected, the RF model with max_features = "sqrt" performed the best, as only a subset (the square root of the total number of features) of the features in considered at each split, and at every subset this subset of different features is random, hence reducing the correlation between trees and giving more reliable averages.

..........

# AdaBoost Classifier
(AdaBoost Classifier is a Boosting algorithm. Boosting also uses ensembles of trees, but instead of training the trees 'independently' on bootstrapped datasets like in bagging, it trains the trees 'sequentially' with each new tree learning from errors of previous trees.) 

Again, like the previous two methods, we defined this AdaBoost Classifier, which learnt from our training data. We then computed how this trained classifier performed/its accuracy on both the training set and the validation set. 

# Choosing the Best Classifier - and retraining it using all the samples - and testing on a test set:
Out of the three methods we looked at, Random Forest was the best model, as this was the one that performed the best/had the best prediction accuracy on the validation set.

# Selecting the most Important Features


