---
tags:
  - Linear-algebra
aliases:
  - Modulus
  - norm
  - length of a vector
---
Modulus of a [[vector]] $\displaystyle \large v$ is defined as:
$$\displaystyle \Huge \begin{eqnarray} 
v &=& \begin{bmatrix} a \\ b \end{bmatrix} \\
|v| &=& \sqrt{a^2+b^2}

\end{eqnarray}$$

And can be understood as its *size*
![[Pasted image 20240118192152.png|450]]


*modulus* of a vector $\displaystyle \large v$ can be obtained using [[dot product]] as well:
$$\displaystyle \Huge \begin{eqnarray} 
|r| &=& \sqrt{r\cdot r} \\
\end{eqnarray}$$

Or a formal definition using [[inner product]]

![[Pasted image 20240119162029.png]]
>[!example]
> Consider the vector $\displaystyle \large \begin{bmatrix}  1 \\ 1 \end{bmatrix}$:
> ![[Pasted image 20250113164803.png|200]]
> 
> and let's get the following [[inner product]]:
> $$\displaystyle \Huge \begin{eqnarray} 
> \langle x, y \rangle &=& x^T \begin{bmatrix} 1 & -\dfrac{1}{2} \\ -\dfrac{1}{2} & 1 \end{bmatrix} y
> \\
> &=& x_1y_1-\dfrac{1}{2}(x_1y_2+x_2y_1) + x_2y_2
> \end{eqnarray}$$
> with the above inner product,
> the norm of vector $\displaystyle \large \begin{bmatrix} 1 \\ 1 \end{bmatrix}$ is:
> $$\displaystyle \Huge \begin{eqnarray} 
> x &=& \begin{bmatrix} 1 \\ 1 \end{bmatrix},
> \\
> \lvert\lvert x \rvert\rvert &=& 1 - \dfrac{1}{2}(1 + 1) + 1
> \\
> &=& 1
> \end{eqnarray}$$

### Properties

1. homogenity:
$$\displaystyle \Huge \begin{eqnarray} 
\lvert \lvert \lambda x \rvert \rvert = \lvert \lambda \rvert * \lvert \lvert x \rvert \rvert
\end{eqnarray}$$
2. [[triangle inequality]]:
$$\displaystyle \Huge \begin{eqnarray} 
\lvert \lvert u+v \rvert \rvert \le 
\lvert \lvert u \rvert \rvert + \lvert \lvert v \rvert \rvert
\end{eqnarray}$$
>[!example]
>![[Pasted image 20250113170536.png|400]]

3. [[Cauchy-Schwarz Inequality]]:
$$\displaystyle \Huge \begin{eqnarray} 
\lvert \langle x,y \rangle \rvert \le \lvert \lvert x \rvert \rvert * \lvert \lvert y \rvert \rvert
\end{eqnarray}$$