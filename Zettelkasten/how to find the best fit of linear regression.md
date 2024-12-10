---
tags:
  - Statistics
aliases:
  - Anscombe's quartet
---

Considering a [[Regression Analysis|Linear Regression]], we can define *residual* $\displaystyle \large d_i$ as:
$$\displaystyle \Huge \begin{eqnarray} 
d_i &=& y_i - \hat{y_i} \\
d_i &=& y_i - (a+xb_i)  \\
&=& y_i - a - bx_i \\
\end{eqnarray}$$

*The way to find the best fit* is to get the min value of the [[Sum of squares errors|RSS]], which is the squared sum of the residuals.

So the best *intercept* a and *slope* $\displaystyle \large b$ are the ones that get the minimum value of *RSS*. This can be found using [[derivative]]:

$$\displaystyle \Huge \begin{eqnarray} 
\text{given the linear regresion: } \\
y &=& b*x + a 
\\ \\
RSS = \chi^2 &=& \sum (y_i - b*x_i + a)
\\ \\
min(RSS) &:=& \dfrac{d}{da} RSS = 0 \text{ and } \dfrac{d}{db} RSS = 0
\end{eqnarray}$$


By consistency with some book material, *RSS will be named here as $\displaystyle \large \chi^2$*, and we will find when the [[gradient]] of [[Sum of squares errors|RSS]] is 0, which is its min:
$$\displaystyle \Huge \begin{eqnarray} 
\nabla \chi ^2 &=& \begin{bmatrix}  
\dfrac{\partial \chi^2}{\partial a} \\
\dfrac{\partial \chi^2}{\partial b}
\end{bmatrix} \\ \\
&=& \begin{bmatrix}  
-2\sum x_i(y_i - b*x_i + a) \\
-2\sum (y_i - b*x_i + a)
\end{bmatrix} 
\\ \\
&=& \begin{bmatrix}  0 \\ 0 \end{bmatrix}
\end{eqnarray}$$

From the second equation we define $\displaystyle \large a$ and from the first $\displaystyle \large b$:
$$\displaystyle \Huge \begin{eqnarray} 
a &=& \bar{y} - b*\bar{x}
\\ \\
b &=& \dfrac{ \sum (x-\bar{x})*y }{ \sum (x-\bar{x})^2 }
\end{eqnarray}$$

>[!info] the uncertainties of a and b can also be found
>$$\displaystyle \Huge \begin{eqnarray} 
>\sigma_a &\approx& \sigma_b * \sqrt{\bar{x}^2 + \dfrac{1}{n}*\sum (x_i - \bar{x})^2} 
>\\
>\sigma_b^2 &\approx& \dfrac{\chi^2}{\sum(x_i - \bar{x})^2(n-2)}
>
>\end{eqnarray}$$

>[!seealso] Anscombe's quartet
> Minimise is not everything, *Anscombe's quartet* shows these 4 plots, all of them with the *same minimum RSS, but with really different fits*:
> ![[Pasted image 20241210004841.png]]
