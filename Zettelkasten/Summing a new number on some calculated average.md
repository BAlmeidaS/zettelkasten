---
tags:
  - math
  - Statistics
---
Considering a [[Average|Mean]] calculated over $\displaystyle \large n-1$ numbers. If a new number $\displaystyle \large x_n$ is introduced, how does it change the average?

$$\displaystyle \Huge \begin{eqnarray} 
given, \\
Average_n &=& \dfrac{x_1+x_2+\dots+x_n}{n} \\
\\
Average_{n-1} &=& \dfrac{x_1+x_2+\dots+x_{n-1}}{n-1} \\
Average_{n-1}*(n-1) &=& x_1+x_2+\dots+x_{n-1}

\\\\
so,
\\
Average_n &=& \dfrac{x_1+x_2+\dots+x_{n-1}+x_n}{n} \\
&=& \dfrac{Average_{n-1}*(n-1)+x_n}{n} \\
&=& \dfrac{Average_{n-1}*n - Average_{n-1} + x_n}{n} \\
&=& \dfrac{Average_{n-1}*n}{n} + \dfrac{-Average_{n-1} + x_n}{n} \\
&=& Average_{n-1} + \dfrac{x_n - Average_{n-1}}{n} \\

\end{eqnarray}$$

And how about the [[Variance]], how will it change?
$$\displaystyle \Huge \begin{eqnarray} 
a &=& 1 \\

\end{eqnarray}$$