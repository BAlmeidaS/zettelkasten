---
tags:
  - Linear-algebra
aliases:
  - trace
  - trace of a matrix
---
The *trace* of a *square matrix* $\displaystyle \large A$, denoted by $\displaystyle \large trace(A)$, is defined to be *the sum of the diagonal entries of $\displaystyle \large A$*.
$$\displaystyle \Huge \begin{eqnarray} 
trace(A) = \sum^n_{i=1}A_{ii}

\end{eqnarray}$$

>[!example]
>$$\displaystyle \Huge \begin{eqnarray} 
>A &=& \begin{bmatrix} a&b&c \\ d&e&f \\ g&h&i \end{bmatrix}
>\\\\
>trace(A) &=& a + e+ i
>\end{eqnarray}$$

Properties:
- *linearity*
$$\displaystyle \Huge \begin{eqnarray} 
trace(A+B) &=& trace(A) + trace(B)
\\
trace(\lambda*C) &=& \lambda * trace(C)
\end{eqnarray}$$
- *invariant under cyclic permutations
$$\displaystyle \Huge \begin{eqnarray} 
trace(AB) = trace(BA)
\end{eqnarray}$$
- sum of [[eigenvalue]]
		The *trace of a matrix is **equal** to the sum of its [[eigenvalue|eigenvalues]]
		
- *Derivative in Matrix Calculus*
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{d}{dx}trace(A) = trace\left(\dfrac{dA}{dx}\right)
\end{eqnarray}$$