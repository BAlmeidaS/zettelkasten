---
tags:
  - Statistics
aliases:
  - Explained Variation
  - Sum of Squares for Regression
---
The **explained variation** of a [[Regression Analysis|Linear Model]] using [[Corrected sums in Regression Models]]. Or *the variation that the model could explain*

It is defined using [[SSXY]] and [[SSX]], or in terms of $\displaystyle \large b$ from [[least-squares]]

$$\displaystyle \Huge \begin{eqnarray} 
SSR &=& \dfrac{SSXY^2}{SSX} \\\\
&\text{or}& \\\\
SSR &=& b*SSXY \\
\end{eqnarray}$$

*SSR* can be defined using the [[Average|Mean]]:
$$\displaystyle \Huge \begin{eqnarray} 
SSR = \sum(\hat{y}_i - \bar{y})^2
\end{eqnarray}$$