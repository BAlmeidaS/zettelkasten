---
tags:
  - Linear-algebra
---
Given a [[matrix]] $\displaystyle \large A$, the inverse of A is defined as $\displaystyle \large A^{-1}$.
It is definition is as following (being $\displaystyle \large I$ the [[identity matrix]])
$$\displaystyle \Huge \begin{eqnarray} 
A^{-1}A &=& I \\
\end{eqnarray}$$

We can understand $\displaystyle \large A^{-1}$ as it *reverses* of [[how matrices transform space|what A did]].
$$\displaystyle \Huge \begin{eqnarray} 
A*r &=& s \\
A^{-1}*A*r &=& A^{-1}*s \\
I*r &=& A^{-1}*s \\
r &=& A^{-1}*s \\
\end{eqnarray}$$

a [[matrix]] has inverse, if and only if, its [[Derterminant]] is different than 0
$$\displaystyle \Huge \begin{eqnarray} 
\exists\ A^{-1} \Longleftrightarrow det(A) \ne 0
\end{eqnarray}$$

---

To find the inverse, you can start with $\displaystyle \large AA^{-1}=I$, and make a sequence of steps to change $\displaystyle \large A^{-1}$ to $\displaystyle \large I$, when you do it on the right side will be the inverse.

For Instance,
$$\displaystyle \Huge \begin{eqnarray} 
A*A^{-1} &=& I \\\\
\begin{bmatrix}  
1 & 1 & 3 \\ 
1 & 2 & 4 \\ 
1 & 1 & 2 
\end{bmatrix}
\begin{bmatrix}  
b_{11} & b_{12} & b_{13} \\ 
b_{21} & b_{22} & b_{23} \\ 
b_{31} & b_{32} & b_{33} \\ 
\end{bmatrix}
&=&
\begin{bmatrix}  
1 & 0 & 0 \\ 
0 & 1 & 0 \\ 
0 & 0 & 1 
\end{bmatrix}
\\\\
\text{to find all the $\displaystyle \large b_{ij}$ get both matrices}
& &
\text{and transform the left side to $I$}
\\\\
\text{1.}
\begin{bmatrix}  
1 & 1 & 3 \\ 
1 & 2 & 4 \\ 
1 & 1 & 2 
\end{bmatrix}
&\rightarrow&
\begin{bmatrix}  
1 & 0 & 0 \\ 
0 & 1 & 0 \\ 
0 & 0 & 1 
\end{bmatrix}\\\\
\text{2.}
\begin{bmatrix}  
1 & 1 & 3 \\ 
0 & 1 & 1 \\ 
0 & 0 & 1 
\end{bmatrix}
&\rightarrow&
\begin{bmatrix}  
1 & 0 & 0 \\ 
-1 & 1 & 0 \\ 
1 & 0 & -1 
\end{bmatrix}\\
\dots\\
\text{final.}
\begin{bmatrix}  
1 & 0 & 0 \\ 
0 & 1 & 0 \\ 
0 & 0 & 1 
\end{bmatrix}
&\rightarrow&
\begin{bmatrix}  
0 & -1 & 2 \\ 
-2 & 1 & 1 \\ 
1 & 0 & -1 
\end{bmatrix}\\\\

A^{-1} &=& 
\begin{bmatrix}  
0 & -1 & 2 \\ 
-2 & 1 & 1 \\ 
1 & 0 & -1 
\end{bmatrix}\\
\end{eqnarray}$$

