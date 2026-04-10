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
We fit decision trees with different depths up to max_depth = 15. These decision trees were trained on/learnt from our training data. We then saw how this (trained) decision tree performed/its accuracy on - both the training set and the validation set - for each different depth (1-15). -> We then took the best max_depth for our decision tree, which was the max_depth for which the decison tree had the best performance/accuracy on the validation set. 

# Random Forest Classifier


# AdaBoost Classifier


# Choosing the Best Classifier - and retraining it using all the samples - and testing on a test set:


# Selecting the most Important Features


