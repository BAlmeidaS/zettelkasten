---
tags:
  - Calculus
---
*The quadratic form can be written as*:
$$\displaystyle \Huge \begin{eqnarray} 
\boldsymbol{x}^T \boldsymbol{M} \boldsymbol{x}
\end{eqnarray}$$

Given a [[multivariable function]] we wish to create a *vectorize way* to express a function that have *a relation between the quadratic variables and its constant*:
$$\displaystyle \Huge \begin{eqnarray} 
f(x,y,z,\dots) 
&=& ax^2 + bxy + cxz + \dots \\
& & + byx + ky^2 + lyz + \dots \\
& & + czx + lzy + uz^2 + \dots \\
& & + \dots \\
\text{(summing equal terms:)}\\
&=& ax^2+2bxy+2cxz + \dots \\
& & + ky^2 + 2lyz + \dots \\
& & + uz^2 + \dots \\
& & + \dots \\
\end{eqnarray}$$

So, we want to express this in terms of [[vector|vectors]] and [[matrix|matrices]]. Given:
- vector $\displaystyle \large \boldsymbol{x}$ (bold) being the vector of the variables
$$\displaystyle \Huge \begin{eqnarray} 
\boldsymbol{x}=
\begin{bmatrix}
x \\
y \\
z \\
\vdots
\end{bmatrix}
\end{eqnarray}$$
- matrix $\displaystyle \large \boldsymbol{M}$ (bold) is a [[symmetric matrix]] with the variables
$$\displaystyle \Huge \begin{eqnarray} 
\boldsymbol{M}=
\begin{bmatrix} 
a & b & c &\dots \\
b & k & l &\dots \\
c & l & u &\dots \\
\vdots & \vdots & \vdots & \ddots
\end{bmatrix}
\end{eqnarray}$$

>[!example] example with 3 variables
with *3 variables* we want to get this formula:
>$$\displaystyle \Huge \begin{eqnarray} 
>ax^2+2bxy+2cxz+dy^2+eyz+fz^2
>\end{eqnarray}$$
>
>The same variable should be obtained as:
>$$\displaystyle \Huge \begin{eqnarray}
>&\boldsymbol{x}^T& \boldsymbol{M} \boldsymbol{x} \\
>\text{being, } \\
>&\boldsymbol{x}&=
>\begin{bmatrix}
>x \\
>y \\
>z \\
>\end{bmatrix} \\
>
>&\boldsymbol{M}&=
>\begin{bmatrix} 
>a & b & c \\
>b & d & e \\
>c & e & f \\
>\end{bmatrix}
>\end{eqnarray}$$
>
>Doing the math:
>$$\displaystyle \Huge \begin{eqnarray} 
>\boldsymbol{x}^T \boldsymbol{M} \boldsymbol{x} 
>&=& 
>\begin{bmatrix} x & y & z 
>\end{bmatrix} 
>\begin{bmatrix} 
>a & b & c \\
>b & d & e \\
>c & e & f \\
>\end{bmatrix}
>\begin{bmatrix}
>x \\
>y \\
>z \\
>\end{bmatrix}
>\\
>&=& 
>\begin{bmatrix} x & y & z 
>\end{bmatrix} 
>\begin{bmatrix} 
>ax & by & cz \\
>bx & dy & ez \\
>cx & ey & fz \\
>\end{bmatrix}
>\\
>&=& ax^2 + bxy + cxz + byx + dy^2 + eyz + czx + ezy + fz^2 \\
>&=& ax^2 + 2bxy + 2cxz + dy^2 + 2eyz + fz^2 \\
>&&&\blacksquare
>
>\end{eqnarray}$$

