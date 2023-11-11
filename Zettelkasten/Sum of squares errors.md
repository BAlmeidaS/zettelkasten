---
tags:
  - Statistics
aliases:
  - Sum of Squares
  - SSE
---
The **unexplained variation** of a [[Regression Analysis|Linear Model]]. Or the *variation that the model could not explain*.

Perhaps the most important single quantity in all statistics. It has multiple interpretations but in its purest form is:
$$\displaystyle \Huge sum\_of\_squares = \sum d_i^2 =\sum\limits^n_{i=1}(y_i-\hat{y_i})^2$$
*SSE is the sum of the squares of the [[Deviation|deviations]]*.

The unit depends on the unit of $\displaystyle \large y$ and it will be that one squared.

*sum of squares always increases with the addition of new data points* (or stays the same if the data point has the value exactly equal to the mean). Usually this is "bad thing", because it is not comparable since it depends on the size of the dataset.

**Degrees of freedom**

Since *SSE*, depends on $\displaystyle \large \hat{y_i}$, which is the predicted value on $\displaystyle \large i$, and $\displaystyle \large \hat{y_i} = a + bx$, so *SSE depends on **a** and **b**, thus the SSE [[Degrees of Freedom]] are $\displaystyle \large n-2$*.

