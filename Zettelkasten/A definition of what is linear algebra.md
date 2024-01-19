---
tags:
  - Linear-algebra
---
Linear algebra **is linear**, because **it just takes input values** and **multiplies them by constants**. So everything is linear.

And it's algebra, that is it's a notation describing mathematical objects and a system of manipulating those notations.

So **linear algebra is a mathematical system for manipulating vectors in the spaces described by vectors**.

---

The example to understand comes from [[First use of Linear Algebra is solving system of equations]]

In practice a system of equations can be understood as a matrix that is a **function** that *operates* over *input vector* and gives *output vectors*.

So, the system,
$$\displaystyle \Huge \begin{eqnarray} 
2a+3b &=& 8 \\
10a+1b &=& 13 \\
\end{eqnarray}$$
Can be rewritten to,
$$\displaystyle \Huge \begin{eqnarray} 
\begin{bmatrix} 2 & 3 \\ 10 & 1 \end{bmatrix}
\begin{bmatrix} a \\ b \end{bmatrix} = 
\begin{bmatrix} 8 \\ 13 \end{bmatrix}
\end{eqnarray}$$
Thus, $\displaystyle \large \begin{bmatrix} 2 & 3 \\ 10 & 1 \end{bmatrix}$ can be interpreted as a **function that transforms** any *input vector* into an *output vector*. 

In this particular case, we are interested in finding what input vector $\displaystyle \large \begin{bmatrix} a \\ b \end{bmatrix}$ can be used to, using this function, be transformed into $\displaystyle \large \begin{bmatrix} 8 \\ 13 \end{bmatrix}$.

This is connected of [[how matrices transform space]]
