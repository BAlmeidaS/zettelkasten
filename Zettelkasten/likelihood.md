---
tags:
  - Statistics
  - machine-learning
aliases:
  - likelihood
  - log likelihood
---
Mathematically speaking, the *likelihood* of a [[Machine Learning]] or *statistical model* with parameters $\displaystyle \large \Theta$ is related to the *probability of all that $\displaystyle \large n$ datapoints occur given those parameters* :
$$\displaystyle \Huge \begin{eqnarray} 
L(\Theta) &=& \prod^n_{i=1} P(x_i \mid \Theta) 
\end{eqnarray}$$

Usually we calculate the *log likelihood*, we can apply *log* on the function without losing any meaning, given that *log is monotone increasing*. 

So, we define as **Log-Likelihood** as:
$$\displaystyle \Huge \begin{eqnarray} 
\log L(\Theta) &=& \log (\prod^n_{i=1} P(x_i \mid \Theta)) \\
&=& \sum^n_{i=1} \log P(x_i \mid \Theta)
\end{eqnarray}$$

Is easier to compute, because it involves summation rather than multiplication