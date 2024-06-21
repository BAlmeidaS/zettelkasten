---
tags:
  - deep-learning
---
Given a [[Graphs|Graph]] $\displaystyle \large G = (V, E)$, learn a function where:

*Task is predict new links based on existing links*
![[Pasted image 20240620220704.png|400]]
At predict time, all node pairs (without existing links) are ranked, and top K node pairs are predicted.

>[!tip] Methodology
> 1. For each pair of nodes $\displaystyle \large (x, y)$, compute score $\displaystyle \large c(x, y)$
> 2. Sort pairs by the decreasing score
> 3. *Predict top* n pairs as new links
> 4. See which of these links actually appear in $\displaystyle \large G_{t_1}$

*The key is to design **features for pairs of nodes**.*
A simple (and bad solution) is to concatenate the [[Node-level Task - Traditional ML methods|features designed to the nodes]]


Two possible formulation of the link prediction:
### 1. links missing at random
Remove a random set of links and then aim to predict them

### 2. links over time
Given a $\displaystyle \large G_{t_0}$ a graph on edges up to time $\displaystyle \large t_0$, output a *ranked list $\displaystyle \large L$* of links that are predicted to appear in $\displaystyle \large G_{t_1}$
- evaluate by measuring $\displaystyle \large n=|E_{new}|$, number of new edges that appeared on time $\displaystyle \large t_1$
- Take top $\displaystyle \large n$ elements of $\displaystyle \large L$ and count correct edges

---
Features (manually designed) that might be useful as descriptors of two-nodes (edges):
- [[Distance-based feature]]
- [[Local neighbourhood overlap]]
- [[Global neighbourhood overlap]]

