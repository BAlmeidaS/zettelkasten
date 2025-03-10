---
tags:
  - Statistics
---
The *log odds* is basically the log of the [[Odds]]:
$$\displaystyle \Huge \begin{eqnarray} 
\log(\text{odds of a var}) = \log\dfrac{p}{1 - p}
\end{eqnarray}$$

being $\displaystyle \large p$ the probability of that variable to be true

>[!note] the inverse operation
>from log odds to probability we can do the inverse
>$$\displaystyle \Huge \begin{eqnarray} 
>&&&log \left(\dfrac{p}{1-p}\right) =& log(odds)
>\\&\iff&
>&\dfrac{p}{1-p} =& e^{log(odds)}
>\\&\iff&
>&p =& (1-p)e^{log(odds)}
>\\&\iff&
>&p =& e^{log(odds)} - pe^{log(odds)}
>\\&\iff&
>&p + pe^{log(odds)} =& e^{log(odds)}
>\end{eqnarray}$$
>so,
>$$\displaystyle \Huge \begin{eqnarray} 
>p = \dfrac{e^{log(odds)}}{1 + e^{log(odds)}}
>\end{eqnarray}$$
> of course this is the same as the [[Sigmoid function]]:
> $$\displaystyle \Huge \begin{eqnarray} 
> f(p) = \dfrac{1}{1 + e^{-p}}
>\end{eqnarray}$$
> 


The idea to *apply log* over odds is **to make it symmetrical around 0**, instead of going from 0 to $\displaystyle \large \infty$, it goes from $\displaystyle \large -\infty$ to $\displaystyle \large \infty$.

*Positive log odds* -> **higher chances to win**
*Negative log odds* -> **higher chances to lose**

![[Pasted image 20231202153541.png]]
