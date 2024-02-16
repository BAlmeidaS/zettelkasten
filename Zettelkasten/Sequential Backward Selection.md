---
tags:
  - machine-learning
aliases:
  - BFS
---
A type of [[feature selection - wrapper methods]]

Similar to [[Sequential Forward Selection|SFS]] but instead of adding feature, each step you *remove features*.

So you start with the [[Types of simplification over Statistics Model|Maximal model]] and each step you remove one of each feature in the model, and using [[cross validation]] you compare them, to *decide by the least important feature to be removed*.
