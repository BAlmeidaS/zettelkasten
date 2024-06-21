---
tags:
  - computer-science
  - machine-learning
aliases:
  - adamic-adar
  - Common neighbours
---
*Local neighbourhood overlap* is a possible feature to measure how much two [[Vertices]] are *close to be connected*, to predict [[Edge-level Task - Graph Neural Networks|if a new edge should be added]].


Score based on the *number of direct shared neighbours between the two nodes $\displaystyle \large v_1$ and $\displaystyle \large v_2$*.

- *Common neighbours*:
$$\displaystyle \Huge \begin{eqnarray} 
|N(v_1) \cap N(v_2)|
\end{eqnarray}$$

- [[Jaccard Similarity|Jaccard's coefficient]]:
$$\displaystyle \Huge \begin{eqnarray} 
\dfrac{|N(v_1)\cap N(v_2)|}{|N(v_1)\cup N(v_2)|}
\end{eqnarray}$$
tries to normalise by the degree of the nodes

- *Adamic-Adar index*:
$$\displaystyle \Huge \begin{eqnarray} 
\sum_{u \in N(v_1) \cap N(v_2)} \dfrac{1}{log(k_u)}
\end{eqnarray}$$
being $\displaystyle \large k_u$ the [[Node Degree]]

---
An overall problem on *Local Neighbourhood overlap* scores is that try to connects nodes that share at least one neighbour (otherwise all the definition evaluate as 0)

---

>[!example]
>![[Pasted image 20240620224317.png|300]]
>
> Score of $\displaystyle \large (A, B)$
>- common neighbours: $\displaystyle \large |\{C\}| = 1$
>
>- jaccard's coefficient: $\displaystyle \large \dfrac{|\{C\}|}{|\{C, D\}|} = \dfrac{1}{2}$
>
>- adamic-adar index: $\displaystyle \large \dfrac{1}{log(k_C)} = \dfrac{1}{log4}$
