---
tags:
  - Statistics
aliases: []
---
The way that two [[Random Variable]] ([[Numerical variables]]) vary together, the way they *co-vary*
$$\displaystyle \Huge \begin{eqnarray} 
Cov(x, y) &=& E[(x-\bar{x})(y-\bar{y})] \\
&=& \dfrac{1}{n-1}\sum\limits^n_{i=1}(x_i - \bar{x})(y_i - \bar{y})
\end{eqnarray}$$

When:
- $\displaystyle \large Cov(x,y) = 0$ we say that the variables, x and y, are **independent***.
- $\displaystyle \large Cov(x,y) > 0$ if $\displaystyle \large x$ increase, y increases.
- $\displaystyle \large Cov(x,y) < 0$ if $\displaystyle \large x$ increase, y decreases.

The Covariance might be understood as an area, a rectangle with sides $\displaystyle \large x - \mu_x$ and $\displaystyle \large y - \mu_y$:
![[Pasted image 20241217183507.png]]


Being $\displaystyle \large E[z]$ the [[Expected Value]].

$$\displaystyle \Huge \begin{eqnarray} 
cov(x, y) &=& E(xy) - E(x\bar{y}) - E(\bar{x}y) + E(\bar{x}\bar{y}) \\
&=& E(xy) - \bar{y}E(x) - \bar{x}E(y) + \bar{x}\bar{y} \\
&=& E(xy) - \bar{y}\bar{x} - \bar{x}\bar{y} + \bar{x}\bar{y} \\
&=& E(xy) - \bar{y}\bar{x} \\
cov(x,y) &=& E(xy) - E(x)E(y) \\
\end{eqnarray}$$

When, $\displaystyle \large x$ and $\displaystyle \large y$ are *uncorrelated*, $\displaystyle \large cov(x,y) = 0$, so $\displaystyle \large E(xy) = E(x)E(y)$.

---

Using the [[Correct sums]] ([[SSXY]]), we have:
$$\displaystyle \Huge \begin{eqnarray} 
cov(x, y) &=& \text{SSXY}\sqrt{\dfrac{1}{(n-1)^2}} \\
\end{eqnarray}$$

---
#### Some examples with Visualisation
>[!example] Complex data
>$$\displaystyle \Huge \begin{eqnarray} 
>Data =
>\begin{bmatrix}  
>1 & 2 \\  5 & 4 \\  -2 & -3 \\  4 & -2 \\  2 & 3 \\  8 & -9 \\ 
>\end{bmatrix}
>\end{eqnarray}$$
>![[Pasted image 20241217184004.png|500]]

>[!example] Straight data
>$$\displaystyle \Huge \begin{eqnarray} 
>Data =
>\begin{bmatrix}  
>1 & 1 \\  -3 & -3 \\  2 & 2 \\  7 & 7 \\
>\end{bmatrix}
>\end{eqnarray}$$
>![[Pasted image 20241217184217.png|500]]

>[!example] Squared data
>$$\displaystyle \Huge \begin{eqnarray} 
>Data =
>\begin{bmatrix}  
>0 & 0 \\  4 & 4 \\  0 & 4 \\  4 & 0 \\
>\end{bmatrix}
>\end{eqnarray}$$
>![[Pasted image 20241217184349.png|500]]

$$\displaystyle \Huge \begin{eqnarray} 
Var(x) = \dfrac{1}{n}*\sum^n(x-\bar{x})^2
\end{eqnarray}$$
$$\displaystyle \Huge \begin{eqnarray} 
Var(y) = \dfrac{1}{n}*\sum^n(y-\bar{y})^2
\end{eqnarray}$$
$$\displaystyle \Huge \begin{eqnarray} 
Cov(x, y) = \dfrac{1}{n}*\sum^n(x-\bar{x})(y-\bar{y})
\end{eqnarray}$$

