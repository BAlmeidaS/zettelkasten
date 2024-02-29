---
tags:
  - machine-learning
aliases:
  - distance matrix
  - similarity matrix
---
A proximity matrix contains *the pairwise indices of proximity of a dataset* $\displaystyle \large D = \{x_1, x_2, \dots, x_n\}$. 

The *proximity can be defined as a [[distance function]]*, and we have a *distance matrix*:
$$\displaystyle \Huge \begin{eqnarray} 
M_{dist}(D) = 
\begin{bmatrix} 
0 & d_{12} & \dots & d_{1n}  \\ 
d_{21} & 0 & \dots & d_{1n}  \\ 
\vdots & \vdots & \ddots & \vdots \\
d_{n1} & d_{n2} & \dots & 0  \\ 
\end{bmatrix}
\end{eqnarray}$$

Or, the *proximity can be defined as a [[Similarity function]]*, and we have a *similarity matrix*:
$$\displaystyle \Huge \begin{eqnarray} 
M_{sim}(D) = 
\begin{bmatrix} 
1 & s_{12} & \dots & s_{1n}  \\ 
s_{21} & 1 & \dots & s_{1n}  \\ 
\vdots & \vdots & \ddots & \vdots \\
s_{n1} & s_{n2} & \dots & 1  \\ 
\end{bmatrix}
\end{eqnarray}$$

This matrix might or might not be [[symmetric matrix]], it depends on the functions.