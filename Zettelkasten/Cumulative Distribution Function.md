---
tags:
  - Statistics
aliases:
  - CDF
---
It is a function that indicates the probability that a [[Random Variable]] $\displaystyle \large X$ will take a value less than or equal to $\displaystyle \large x$. 

Mathematically, for a [[Continuous variable]], the *CDF $\displaystyle \large F(x)$* is the integral of its probability density function $\displaystyle \large f(t)$ from the lower bound of the distribution (which could be $\displaystyle \large -\infty$) up to $\displaystyle \large x$:
$$\displaystyle \Huge CDF = F(x)=P(X\le x) = \int\limits^x_{-\infty}f(t)dt$$
For a [[Categorical variable|Discrete variable]]
$$\displaystyle \Huge CDF = F(x)=P(X\le x) = \sum\limits_{t \le x}P(X=t)$$