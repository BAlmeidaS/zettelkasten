---
tags:
  - machine-learning
---
*Bagging* is a type of [[Ensemble method]]. It is a short for *Bootstrap Aggregating*.

*Bagging* involves training multiple models of the *same type* on different subsets of the training dataset.  
  
These subsets are created by randomly sampling with replacement from the training set, primarily on the rows of the dataset, process also known as [[Bootstrap]].
  
The final prediction is made by *averaging the predictions* (for regression tasks) or by a *majority vote* (for classification tasks).  
  
A well-known example of a bagging ensemble is the [[Random Forest]] algorithm.