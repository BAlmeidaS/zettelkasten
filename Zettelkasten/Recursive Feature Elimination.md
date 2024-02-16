---
tags:
  - machine-learning
---
A type of [[feature selection - wrapper methods]]

The idea is similar to [[Sequential Backward Selection|BFS]], but you remove the features not by training many model, but step by step *removing the last important feature*.

If the model chosen is a linear model, you can use the [[p-value]] of the coefficient to chose in each step what feature should be removed



