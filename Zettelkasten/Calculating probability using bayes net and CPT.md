If the Bayes Net contains $\displaystyle \large n$ variables, $\displaystyle \large X_1, \dots, X_n$, an entry in the [[Joint Probability Distribution]]:
$$\displaystyle \Huge \begin{eqnarray} 
P(x_1, \dots,x_2) &=& P(x_1\land\dots\land x_n) \\
&=& \prod^n_{i=1}\theta(x_i\mid parents(X_i)) \\
&& \text{being $parents(X_i)$ the parents defined on bayes net}
\end{eqnarray}$$

---
Considering the following [[Bayesian Network|Bayes Net]] with [[Conditional probability table]]
![[Pasted image 20231016015522.png|500]]

what is the $\displaystyle \large P(j,m,a,\lnot b,\lnot e)$?

$$\displaystyle \large \begin{eqnarray} 
P(j,m,a,\lnot b, \lnot e) &=& 
P(j\mid a) * P(m\mid a) * P(a\mid \lnot b \land \lnot e) * P(\lnot b) * P(\lnot e)
\\ &=& 
0.9 * 0.7 * 0.001 * 0.999 * 0.998

\end{eqnarray}$$