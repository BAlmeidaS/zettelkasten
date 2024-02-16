---
tags:
  - machine-learning
aliases:
  - SFS
---
A type of [[feature selection - wrapper methods]]

it is a [[greedy algorithm]] that attempts to find the “optimal” feature subset by iteratively selecting features based on the classifier performance.

We start with an empty feature subset and add one feature at the time in each round; this one feature is selected from the pool of all features that are not in our feature subset, and it is the feature that – when added – results in the best classifier performance. 

Using [[cross validation]] this approach is feasible, though costy! 

>[!eexample]
> 1. If you have 10 features that are not in the set of "features already in use" this means that 10 new models will be fit.
> 2. Each one with the features on the set of "features already in use" + each one of the remaining features.
> 3. Then they these 10 will be compared and one feature will be chosen to be added.
