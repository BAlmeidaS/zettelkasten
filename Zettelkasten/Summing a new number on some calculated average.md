---
tags:
  - math
  - Statistics
cssclasses:
  - wider_page.css
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
&=& Average_{n-1} + \dfrac{x_n - Average_{n-1}}{n} \\\\
so,\\
\overline{x_n} &=& \overline{x_{n-1}} + \dfrac{x_n - \overline{x_{n-1}}}{n}

\end{eqnarray}$$

And how about the [[Variance]], how will it change?

$$\displaystyle \Huge \begin{eqnarray} 
\sigma^2_{n-1} &=& \dfrac{\sum\limits^{n-1} (x-\overline{x_{n-1}})}{n-1}\\
\sigma^2_{n} &=& \dfrac{\sum\limits^n (x-\overline{x_n})}{n} \\
\\\\

\sigma^2_{n} &=& \dfrac{\sum\limits^n 
\left(x 
- \overline{x_{n-1}} 
- \dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2} {n}
\\\\ && \text{using }(a-b)^2 = a^2 - 2ab + b^2,
\\
&=& \dfrac{\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
-2\left(
(x - \overline{x_{n-1}})
* (\dfrac{x_n - \overline{x_{n-1}}}{n})
\right)^2
+\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}{n}
\\\\&&\text{separting } \Sigma s,
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
-2
\overbrace{
\sum\limits^n 
\left(
\overbrace{
(x - \overline{x_{n-1}})
}^{\text{around the mean}}
*
\overbrace{
(\dfrac{x_n - \overline{x_{n-1}}}{n})
}^{\text{not depent of i}}
\right)^2
}^{\text{this part is 0}}
+
\sum\limits^n 
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}{n}
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
+
\overbrace{
\sum\limits^n 
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}^{\text{not dependent on i, only will occur n times}}
}{n}
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
}{n}
+
\dfrac{
n*
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}{n}
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
}{n}
*
\left(
\dfrac{n-1}{n-1}
\right)
+
\dfrac{
\cancel{n}*
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
}{\cancel{n}}
\\
&=& \dfrac{
\sum\limits^n 
\left(
x - \overline{x_{n-1}} 
\right)^2
}{n-1}
*
\left(
\dfrac{n-1}{n}
\right)
+
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
\\
&=& 
\sigma^2_{n-1}
*
\left(
\dfrac{n-1}{n}
\right)
+
\left(
\dfrac{x_n - \overline{x_{n-1}}}{n}
\right)^2
\end{eqnarray}$$
