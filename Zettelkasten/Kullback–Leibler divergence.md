---
tags:
  - machine-learning
aliases:
  - kl divergence
---
*KL divergence* is a measure of how much two distributions are close to each other.

In information theory, kl divergence measures *the extra amount of information required to encode samples from the true distribution $\displaystyle \large P$ when using the approximate distribution $\displaystyle \large Q$*. 

![[Pasted image 20240614164243.png|400]]

On *discrete* space:
$$\displaystyle \Huge \begin{eqnarray} 
D_{KL}(P \parallel Q) = \sum_{x}P(x)\log\dfrac{P(x)}{Q(x)}
\end{eqnarray}$$
On *continuous* space
$$\displaystyle \Huge \begin{eqnarray} 
D_{KL}(P \parallel Q) = \int_{-\infty}^{\infty}p(x)\log\dfrac{p(x)}{q(x)} dx
\end{eqnarray}$$

- $\displaystyle \large P(x)$ is the *true distribution*
- $\displaystyle \large Q(x)$ is the *approximate distribution*

- **KL divergence is asymmetric!**
$$\displaystyle \Huge \begin{eqnarray} 
D_{KL}(P \parallel Q) \ne
D_{KL}(Q \parallel P)
\end{eqnarray}$$

- The **best values is $\displaystyle \large 0$**, which means that $\displaystyle \large P$ and $\displaystyle \large Q$ are the same! or there is no divergence between them
$$\displaystyle \Huge \begin{eqnarray} 
D_{KL}(P \parallel Q) \in [0, \infty[
\end{eqnarray}$$
