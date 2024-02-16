---
tags:
  - machine-learning
---
*L2 regularization* is also known as *ridge*.

Basically, it add a penalty on the [[loss function]] equal to the *square of the coefficients*:

$$\displaystyle \Huge \begin{eqnarray} 
Loss &=& Pure\_Loss + \lambda\sum\beta_j^2

\end{eqnarray}$$

$\displaystyle \large \lambda$ is a [[Hyperparameters of the model|Hyperparameter]] of the model, it sets how much of the penalty will be given for the coefficients.

In opposite of [[L1 Regularisation|L1]], *L2 does not work well as feature selection*, because it does not reduce the coefficients to zero.

>[!hint] Math interpratation
>The set of points for which the L1 regularization term is constant forms a diamond shape in two dimensions (or a higher-dimensional equivalent, often called a "cross-polytope," in more dimensions).
>This is because the absolute value function $\displaystyle \large |x|$ grows linearly in both the positive and negative directions from the origin, forming sharp corners (or edges) at each axis. In two dimensions, this constraint region looks like a square that has been rotated 45 degrees (hence, often referred to as a "diamond").
>
>*the consequence*: The diamond-shaped constraint of L1 regularization means that optimization paths are more likely to hit the axes (where one of the weights becomes exactly zero), leading to sparsity in the model coefficients. This property is particularly useful for feature selection.

