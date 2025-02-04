---
tags:
  - machine-learning
aliases:
  - ridge regularisation
---
*L2 regularization* is also known as *ridge*.

Basically, it add a penalty on the [[Cost function]] equal to the *square of the coefficients*:

$$\displaystyle \Huge \begin{eqnarray} 
Loss &=& Pure\_Loss + \lambda\sum\beta_j^2
\end{eqnarray}$$

$\displaystyle \large \lambda$ is a [[Hyperparameters of the model|Hyperparameter]] of the model, it sets how much of the penalty will be given for the coefficients.

>[!note] machine learning lingo
> It is said that L2 regularisation *adds bias* into the model, *reducing the variance*, therefore.

>[!important]
>**The intercept is not including on the penalty!**

In opposite of [[L1 Regularisation|L1]], *L2 does not work well as feature selection*, because it does not reduce the coefficients to zero.

>[!hint] Math interpratation
> The set of points for which the L2 regularization term is constant forms a circle in two dimensions (or a sphere in three dimensions, and so forth in higher dimensions). This is because the sum of squares $\displaystyle \large \beta_1^2 + \beta_2^2 = constant$ defines the equation of a circle centered at the origin. The L2 penalty increases quadratically as we move away from the origin, which results in smooth, rounded contours without any sharp corners or edges.
> 
>*the consequence*: The circular (or spherical) constraint of L2 regularization encourages the weights to be small but does not necessarily drive them to zero. This results in models where the weight values are distributed more smoothly and none are exactly zero
>
>![[Pasted image 20240216180111.png]]

![[Pasted image 20250204165759.png|400]]

