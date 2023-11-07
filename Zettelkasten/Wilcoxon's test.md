---
tags:
  - Statistics
---
[[Non-parametric Method|non-parametric]] version of [[Student's t test]]

We use *Wilcoxon's test* with only 1 constant / assumption:
1. The samples are indepentents.

It is a test to *compare means* of 2 distributions. 
[[Null Hypothesis|H0]]: Means are the same
[[Alternative Hypothesis|H1]]: Means are different

*Wilcoxon's test* is defined by the following procedure:
1. Aggregate both distribution in one unique array, keep the labels of each entry
2. Sort this array
3. Assign a rank for each value - if two or more values are equal [[ties while ranking an array]]
4. Ranks are added up for each one of the samples. So you will have a:
$$\displaystyle \Huge \begin{eqnarray} 
S_A = Sum(rank[label == A]) \\
S_B = Sum(rank[label == B]) \\
\end{eqnarray}$$
5. Get the smallest between $\displaystyle \large S_A$ and $\displaystyle \large S_B$:
$$\displaystyle \Huge S_{\text{final}} = min(S_A, S_B)$$
6. Find the $\displaystyle \large S_{\text{ref}}$ in a [Wilcoxon rank sums table](https://real-statistics.com/statistics-tables/wilcoxon-rank-sum-table-independent-samples/) - You will need the $\displaystyle \large \alpha$ that you want, and the size of both distributions $\displaystyle \large n_A$  and $\displaystyle \large n_B$.
*For instance, if $\displaystyle \large n_A=10$ and $\displaystyle \large n_B = 10$ and I want $\displaystyle \large \alpha=.05$, then, $\displaystyle \large S_{\text{ref}} = 78$*
7. We reject [[Null Hypothesis|H0]] if $\displaystyle \large S_{\text{final}} \le S_{\text{ref}}$ :
$$\displaystyle \Huge \begin{eqnarray} 
S_{\text{final}} \le S_{\text{ref}} &\rightarrow& \text{reject }H0 \\
S_{\text{final}} \gt S_{\text{ref}} &\rightarrow& \text{fail to reject }H0

\end{eqnarray}$$
