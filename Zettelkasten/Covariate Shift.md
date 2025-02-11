---
tags:
  - machine-learning
---
A common problem in [[Machine Learning]], when the [[Data in machine learning|data]] used on training changes compared to the [[Data in machine learning|data]] used on test (or production).

In other words, the statistical properties of the data may differ between the training and testing datasets. 

This can be problematic because models are typically trained assuming that the training data and testing data are drawn from the same distribution. *When there's a shift in the distribution, the model may not perform well on the testing data because it hasn't learned to generalise to the new distribution*.

---

*Covariate shift means that the distribution of some variables are dependent on another variable*
