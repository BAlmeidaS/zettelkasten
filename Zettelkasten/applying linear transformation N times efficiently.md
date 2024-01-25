---
tags:
  - Linear-algebra
---
If the transformation $\displaystyle \large T$ has enough [[eigenvector|eigenvectors]] to create an [[Eigenbasis]] $\displaystyle \large E_b$, you can change the transformation using this [[Eigenbasis]].

$$\displaystyle \Huge \begin{eqnarray} 
E_b &=& 
\begin{bmatrix}  
\text{eigenvec}_1 &
\text{eigenvec}_2 &
\cdots &
\text{eigenvec}_n \\ 
\vdots & \vdots & \cdots & \vdots
\end{bmatrix}
\end{eqnarray}$$

And the transformation can be redefined as:
$$\displaystyle \Huge \begin{eqnarray} 
T_{diagonal} &=& E_b^{-1}*T*E_b \\
\end{eqnarray}$$
Another way to see is the same thing (_Imperium College way, rather than 3blue1brown_):
$$\displaystyle \Huge \begin{eqnarray} 
T&=& E_b*T_{diagonal}*E_b^{-1} \\
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

Therefore, if we have to compute $\displaystyle \large T^n$:
$$\displaystyle \Huge \begin{eqnarray} 
T&=& E_b*T_{diagonal}*E_b^{-1} \\\\

T^2 &=& E_b*T_{diagonal}*E_b^{-1}*E_b*T_{diagonal}*E_b^{-1} \\
&=& E_b*T_{diagonal}*T_{diagonal}*E_b^{-1} \\
&=& E_b*T_{diagonal}^2*E_b^{-1} \\\\

T^n &=& E_b*T_{diagonal}^n*E_b^{-1} \\
\end{eqnarray}$$

![[Pasted image 20240125185719.png|300]]