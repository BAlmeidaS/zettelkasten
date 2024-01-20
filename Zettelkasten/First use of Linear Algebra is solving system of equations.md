---
tags:
  - Linear-algebra
---
System of equations can be modelled as an operation of vectors and matrices

$$\displaystyle \Huge \begin{eqnarray} 
3x + 2y &=& 8 \\
7x + y &=& 15 \\
\end{eqnarray}$$



Can be written as

$$\displaystyle \Huge \begin{eqnarray} 
\begin{bmatrix} 3 & 2 \\ 7 & 1 \end{bmatrix} *
\begin{bmatrix} x \\ y  \end{bmatrix} = 
\begin{bmatrix} 8 \\ 15  \end{bmatrix}
\end{eqnarray}$$

---

>[!Python]
>The following system can be solved using numpy
>![[Pasted image 20240120165321.png|200]]
>```python
>import numpy as np
>
> A = [[4, 6, 2], [3, 4, 1], [2, 8, 13]]
> s = [9, 7, 2] 
> 
> r = np.linalg.solve(A, s)
> ```
