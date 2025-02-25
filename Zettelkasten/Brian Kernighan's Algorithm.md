---
aliases:
  - cancel the most right 1 from a binary number
---
The idea of this algorithm is to *turn off the **rightmost** 1 in a binary number*.

$$\displaystyle \Huge \begin{eqnarray} 
n = 100010\underline{1}00
\\
n = 100010\underline{0}00
\end{eqnarray}$$

to do this the following operation must be done:
$$\displaystyle \Huge \begin{eqnarray} 
n\ \&\ (n-1)
\end{eqnarray}$$

so,
$$\displaystyle \Huge \begin{eqnarray} 
&& 100010100
\\
\&\ && \underline{100010011}
\\
&& 100010000
\end{eqnarray}$$

