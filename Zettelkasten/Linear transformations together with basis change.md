---
tags:
  - Linear-algebra
---
We can use [[linear transformation]] to change the basis of the space, but we can also use to change the space as we want.

Sometimes, we have a space $\displaystyle \large S$ that does not have the common [[unit vector|unit vectors]] that we know ($\displaystyle \large \hat{i}$, $\displaystyle \large \hat{j}, ...$), and we want to apply a transformation to rotate this space 45 degrees. Though we don't know how to rotate this space, we know how to rotate the common space with the common [[unit vector|unit vectors]], $\displaystyle \large T$ does this:
$$\displaystyle \Huge \begin{eqnarray} 
T = \begin{bmatrix} 1&-1 \\ 1&1\end{bmatrix}
\end{eqnarray}$$

Given a transformation $\displaystyle \large B$ that changes from this [[basis]] to the common basis with the $\displaystyle \large \hat{i}$ (and the others common unit vectors). We can rotate it applying the following transformation
$$\displaystyle \Huge \begin{eqnarray} 
B^{-1}*T*B
\end{eqnarray}$$

We know that when we [[combine linear transformations]], we **must read from right to left**. So the way to interpret this transformation is:
1. we change from "this different basis" to "normal word", using $\displaystyle \large B$
2. we rotate the space 45 degrees, using $\displaystyle \large T$
3. we change it back from "normal world" to "this different basis", using $\displaystyle \large B^{-1}$