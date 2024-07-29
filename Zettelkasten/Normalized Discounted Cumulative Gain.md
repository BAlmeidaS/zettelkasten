---
tags:
  - machine-learning
aliases:
  - NDCG
---
*NDCG* is a *ranking quality metric*. It compares [[Ranking an array|Ranks]] to an ideal order where all relevant items are at the top of the list.

*NDCG* has a paramater called $\displaystyle \large k$, which is the *cutoff point* (list length) while evaluating ranking quality - basically *NDCG will evaluate how well the $\displaystyle \large k$ top items are posistioned*
![[Pasted image 20240729150843.png|400]]

Key Concepts:
1. *Relevance* - $\displaystyle \large Rel_i$ : Score indicating *how relevant a particular result is for a given query*.
2. *Cumulative Gain* - $\displaystyle \large CG_k$ : The *sum* of the *releance scores of results up to a certain rank*
$$\displaystyle \Huge \begin{eqnarray} 
CG_k = \sum^k_{i=1}Rel_i
\end{eqnarray}$$
3. *Discounted Cumulative Gain* - $\displaystyle \large DCG_k$ : adjusts the *Cumulative gain*  by taking ito account the position of the result, usually by $\displaystyle \large \log_2$ of the position
$$\displaystyle \Huge \begin{eqnarray} 
DCG_k = \sum^k_{i=1}\dfrac{Rel_i}{\log_2(i+1)}
\end{eqnarray}$$
4. *Ideal DCG* - $\displaystyle \large IDCG_k$ : this is the *ideal ranking*, where the results are perfectly ordered.


Finally, we have $\displaystyle \large NDCG_k$:
$$\displaystyle \Huge \begin{eqnarray} 
NDCG_k = \dfrac{DCG_k}{IDCG_k}
\end{eqnarray}$$

*$\displaystyle \large NDCG$ close to **1** means **high quality ranking**, whereas close to **0** means **low quality ranking***.

>[!example]
>![[Pasted image 20240729151818.png]]
