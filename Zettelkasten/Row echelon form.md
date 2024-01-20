---
tags:
  - Linear-algebra
---
A [[matrix]] is in *row echelon form* if:
- all rows having only zero entries are at the bottom
- the leading entry (pivot) is on the right of every row above


General form, one example may be:
$$\displaystyle \Huge \begin{eqnarray} 
\begin{bmatrix}  
1 & a_0 & a_1 & a_2 \\ 
0 & 0 & a_3 & a_4 \\ 
0 & 0 & 0 & a_5 \\ 
\end{bmatrix}
\end{eqnarray}$$

Usually to [[First use of Linear Algebra is solving system of equations|find solutions to equation systems]], the solution passes through the process to put the square [[matrix]] in *row echelon form*. For instance a system of 3 equations will be transformed into:
$$\displaystyle \Huge \begin{eqnarray} 
\begin{bmatrix}  
1 & a_0 & a_1 \\ 
0 & 1 & a_2 \\ 
0 & 0 & 1 \\ 
\end{bmatrix}
\end{eqnarray}$$