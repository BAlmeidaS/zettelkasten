---
tags:
  - machine-learning
---
Tree models ([[xgboost]], [[random forest]], [[decision tree]]) have a side effect that is given the *feature importance*, thus it can be used as [[Feature Selection]].

The key idea here is [[information gain]]:

In broad terms, tree models sort features based on how much information each feature provides to explain the variance (or, more generally, the uncertainty or impurity) in the target variable.

This sorting is reflected in the calculation of feature importance scores within these models. The key idea is that features that lead to the largest reduction in uncertainty or impurity when used to split the data are considered more important.