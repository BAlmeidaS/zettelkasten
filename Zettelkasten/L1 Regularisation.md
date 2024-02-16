---
tags:
  - machine-learning
aliases:
  - L1
  - lasso regularization
---
*L1 regularization* is also known as *lasso*, that stands for Least Absolute and Selection Operator.

Basically, it add a penalty on the [[loss function]] equal to the *absolute value of the magnitude of the coefficients*.

$$\displaystyle \Huge \begin{eqnarray} 
Loss &=& Pure\_Loss + \lambda\sum|\beta_j|

\end{eqnarray}$$

$\displaystyle \large \lambda$ is a [[Hyperparameters of the model|Hyperparameter]] of the model, it sets how much of the penalty will be given for the coefficients.

L1 reg has some *special features*:
- It can result in [[sparse vector|sparse]] models, with few coefficients (some zeros) - In the jargon *it shrinks the less important feature’s coefficient to zero thus, removing some features*.
- Good when it has a *high number of features*
