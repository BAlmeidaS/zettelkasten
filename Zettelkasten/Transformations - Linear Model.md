---
tags:
  - Statistics
---
There are some *classical transformations* that you should try after the classical $\displaystyle \large y = a + bx$ [[Regression Analysis|Linear Model]]:

|     | transformation | formula                                     |
| --- | -------------- | ------------------------------------------- |
| 1   | log X          | $\displaystyle \large y = a + b*ln(x)$      |
| 2   | log Y          | $\displaystyle \large y = exp(a + bx)$     |
| 3   | asymptotic     | $\displaystyle \large y = \dfrac{ax}{1+bx}$ |
| 4   | reciprocal     | $\displaystyle \large y = a + \dfrac{b}{x}$ |
| 5   | power law      | $\displaystyle \large y = ax^b$      |
| 6   | exponential    | $\displaystyle \large y = ae^{bx}$      |
![[Pasted image 20231111185715.png|600]]

Or even *Polynomial regression* - using only one explanatory variable, we create function like
$$\displaystyle \Huge y = a+bx+cx^2+dx^3+\ldots$$
![[Pasted image 20231111192129.png|600]]

>[!R lang]
>remember to use the function `I` stands for "as is" and *allows arithmetic operator like `^`
>```R
>polinomal_model <- lm(tgt ~ x + I(x^2), df)
> ```
