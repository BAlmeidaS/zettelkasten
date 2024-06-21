---
tags:
  - machine-learning
---
A way to define [[Shallow encoder embedding]] is via *Random Walk*.

The idea here defining the [[Decoder - Node Embedding|decoder]] as the [[softmax function|softmax]] of the [[inner product]] of the [[embedding]] $\displaystyle \large z_u, z_v$:
$$\displaystyle \Huge \begin{eqnarray} 
DEC(z_u, z_v) &=& softmax(z_u^T\cdot z_v) \\
&=& \dfrac{e^{z_u^Tz_v}}{\sum_{v_k \in V} e^{z_u^T\cdot z_v}} \\
\end{eqnarray}$$
And this $\displaystyle \large DEC$, is the approximation of the [[Similarity function|similarity]] that will be the *probability of visiting $\displaystyle \large v$ on a length $\displaystyle \large T$ random walk starting at node $\displaystyle \large u$*
$$\displaystyle \Huge \begin{eqnarray} 
DEC(z_u, z_v) &=& softmax(z_u^T\cdot z_v) \\
&=& \dfrac{e^{z_u^Tz_v}}{\sum_{v_k \in V} e^{z_u^T\cdot z_v}} \\
&\approx& p_{G, T}(v\mid u)
\end{eqnarray}$$

Thus, the goal is to minimise the *softmax* using [[Cross-entropy|cross-entropy loss]]:
$$\displaystyle \Huge \begin{eqnarray} 
L &=& - \sum_{u,v} \log(DEC(z_u, z_v))
\end{eqnarray}$$

To find the minimum of this loss: [[Gradient Descent]] using as the *datapoints the nodes that appeared connected on the random walk*

>[!hint] Explanation how cross-entropy become the final form of the loss function
>$$\displaystyle \Huge \begin{eqnarray} 
>H(p, q) = - \sum_{u,v} p(v\mid u) \log q(v \mid u)
>\end{eqnarray}$$
>- $\displaystyle \large p(v \mid u)$: *true probability distribution* of context nodes $\displaystyle \large v$ given node $\displaystyle \large u$. It is 1 if $\displaystyle \large v$ is actually observed in the context of $\displaystyle \large u$ on the random walk, and 0 otherwise.
>- $\displaystyle \large q(v \mid u)$: *predicted probability distribution* from the [[softmax function|softmax]]
>$$\displaystyle \Huge \begin{eqnarray} 
>H(p, q) = - \sum_{u,v} p(v\mid u) \log q(v \mid u)
>\end{eqnarray}$$
>we can remove $\displaystyle \large p(v\mid u)$ because either will be 0 (summing 0) or 1 and adding nothing.
>$$\displaystyle \Huge \begin{eqnarray} 
>H(p, q) &=& - \sum_{u,v} \log q(v \mid u) \\
>&=& - \sum_{u,v} \log softmax(z_u^T \cdot z_v) \\
>&=& - \sum_{u,v} \log\left(\dfrac{e^{z_u^Tz_v}}{\sum_{v_k \in V}e^{z_u^T\cdot z_v}}\right) \\
>&=& - \sum_{u,v} \log(DEC(z_u, z_v))
>\end{eqnarray}$$
