---
tags:
  - Linear-algebra
---
The [[matrix]] $\displaystyle \large A$ can transform the [[vector]] $\displaystyle \large v$ as the following:
$$\displaystyle \Huge \begin{eqnarray} 
A * v &=& v^\prime \\
\end{eqnarray}$$

if we have a [[basis]] of $\displaystyle \large e_i$ vectors. We can transform this whole basis by defining the primes of the basis:
$$\displaystyle \Huge \begin{eqnarray} 
\displaystyle \large A*e_i &=& e^\prime_i,\ \forall e_i

\end{eqnarray}$$

If we transform the basis, *we can just apply the basis transformed (all $\displaystyle \large e^\prime_i$) on $\displaystyle \large v$ to get $\displaystyle \large v^\prime$*, way easier than applying the full transformation of A to v

---

An example can help to understand. Given:
$$\displaystyle \Huge \begin{eqnarray} 
A &=& \begin{bmatrix} 2 & 3 \\ 10 & 1\end{bmatrix}\\\\
v &=& \begin{bmatrix} 3 \\ 2 \end{bmatrix}
\end{eqnarray}$$


we can find $\displaystyle \large v^\prime$ as:
$$\displaystyle \Huge \begin{eqnarray} 
v^\prime &=& \begin{bmatrix} 2 & 3 \\ 10 & 1\end{bmatrix}
* \begin{bmatrix} 3 \\ 2 \end{bmatrix} = \begin{bmatrix} 12 \\ 32 \end{bmatrix}
\end{eqnarray}$$

**But we can also transform the space**, in this case the basis $\displaystyle \large e_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$ and $\displaystyle \large e_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$:
$$\displaystyle \Huge \begin{eqnarray} 
e_1^\prime &=& \begin{bmatrix} 2 & 3 \\ 10 & 1\end{bmatrix}
* \begin{bmatrix} 1 \\ 0 \end{bmatrix} = \begin{bmatrix} 2 \\ 10 \end{bmatrix}
\\ \\
e_2^\prime &=& \begin{bmatrix} 2 & 3 \\ 10 & 1\end{bmatrix}
* \begin{bmatrix} 0 \\ 1 \end{bmatrix} = \begin{bmatrix} 3 \\ 1 \end{bmatrix}
\end{eqnarray}$$

and $\displaystyle \large v^\prime$:
$$\displaystyle \Huge \begin{eqnarray} 
v^\prime &=& \begin{bmatrix} 2 & 3 \\ 10 & 1\end{bmatrix}
* \begin{bmatrix} 3 \\ 2 \end{bmatrix} 
\\\\ &=&
\begin{bmatrix} 2 & 3 \\ 10 & 1\end{bmatrix}
* \left(
3 * \begin{bmatrix} 1 \\ 0 \end{bmatrix}
+ 2 * \begin{bmatrix} 0 \\ 1 \end{bmatrix}
\right)
\\\\ &=& 
3 * \left(
\begin{bmatrix} 2 & 3 \\ 10 & 1\end{bmatrix}
\begin{bmatrix} 1 \\ 0 \end{bmatrix}
\right)
+ 2 * \left(
\begin{bmatrix} 2 & 3 \\ 10 & 1\end{bmatrix}
\begin{bmatrix} 0 \\ 1 \end{bmatrix}
\right)
\\\\ &=& 
3*e_1^\prime + 2*e_2^\prime
\\\\
v^\prime &=& 
3 * \begin{bmatrix} 2 \\ 10 \end{bmatrix}
+ 2 * \begin{bmatrix} 3 \\ 1 \end{bmatrix}
= \begin{bmatrix} 12 \\ 32 \end{bmatrix}
\end{eqnarray}$$
