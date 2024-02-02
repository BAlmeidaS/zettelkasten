---
tags:
  - Linear-algebra
aliases:
  - element-wise product
  - hadamard product
  - pointwise
---
The *element-wise product* demands *2 [[matrix|matrices]] with the same size*, the result will be the multiplication of item by item:
$$\displaystyle \Huge \begin{eqnarray} 
A \odot B &=& C 
\\\\
\text{for instance,} \\
\begin{bmatrix} 
1 & 2 & 3\\
0 & 2 & 4\\
\end{bmatrix}
\odot
\begin{bmatrix} 
3 & 2 & 1\\
1 & 1 & 1\\
\end{bmatrix}
&=&
\begin{bmatrix} 
1\times3 & 2\times2 & 3\times1\\
0\times1 & 2\times1 & 4\times1\\
\end{bmatrix}\\
&=&
\begin{bmatrix} 
3 & 4 & 3\\
0 & 2 & 4\\
\end{bmatrix}
\end{eqnarray}$$
