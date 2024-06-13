---
tags:
  - Statistics
---
The *geometric distribution* is the [[Probability Distributions|probability distribution]] of getting a number $\displaystyle \large Y = X - 1$ of failures before you get some success.

$\displaystyle \large X$ in this case is the *Bernoulli trials* needed to get one success

The [[Probability Mass Function|PMF]] is $\displaystyle \large (1-p)^{1-k} * p$, being $\displaystyle \large p$ the *probability of success* and $\displaystyle \large k$ the *number of times that you failed*.

The [[Expected Value]] can be calculated as:
(we will use [[sum of geometric series]] to expand the *expected value*)

$$\displaystyle \Huge \begin{eqnarray} 
X &\sim& Geometric(p)
\\ \\
\mathbb{E(X)} &=& k * \mathbb{p}(x=k)
\\
&=& \sum^{\infty}_{k=1} k * (1-p)^{k-1} * p
\\
&& (\text{if you differentiate sum of geometric series})
\\
&=& \dfrac{p}{p^2}
\\
&=& \dfrac{1}{p}
\end{eqnarray}$$

