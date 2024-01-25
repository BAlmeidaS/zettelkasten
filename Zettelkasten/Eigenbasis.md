---
tags:
  - Linear-algebra
---
[[linear transformation|linear transformations]] that have enough [[eigenvector|eigenvectors]] to spam the space, can be changed to use those [[eigenvector|eigenvectors]] as [[basis]], the *eigenbasis*.

The idea is to create a matrix $\displaystyle \large E_b$ that has in each column one vector of the *eigenbasis* (they must be [[linear independence|linear independent]]). If the transformation has enough [[eigenvector|eigenvectors]] to define the *eigenbasis*, we can change the transformation to be a [[diagonal matrix]]:
$$\displaystyle \Huge \begin{eqnarray} 
T_{diagonal} &=& E_b^{-1}*T*E_b \\
\end{eqnarray}$$

$\displaystyle \large T_{diagonal}$ is composed by the [[eigenvalue|eigenvalues]] of the [[eigenvector|eigenvectors]] chose, in its diagonal

$$\displaystyle \Huge \begin{eqnarray} 
T_{diagonal} = \begin{bmatrix}  
\lambda_0 & 0 & \dots & 0 \\ 
0 & \lambda_2 & \dots & 0 \\ 
\vdots & \vdots& \ddots &\vdots\\
0 & 0 & \dots & \lambda_n \\ 
\end{bmatrix}
\end{eqnarray}$$

*The most powerful characteristic of this is [[applying linear transformation N times efficiently]]*