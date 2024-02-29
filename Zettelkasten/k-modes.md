---
tags:
  - machine-learning
---
*K-modes* is a [[Partitional clustering]], more specifically a [[centre-based clustering]].

It extends the idea of [[k-means]] but for [[categorical variable]], using the [[Simple Matching distance]].

The centres, or *modes*, are represented by the most common category values for each feature within the cluster.

The update mechanism is by choosing the category values that are most frequent ([[Mode]]) among the points assigned to the cluster.

The [[objective function]] is the [[Simple Matching distance]], and the goal is to minimise it.

>[!success] advantages
>- As efficient as k-means
>- Robustness - it provides a cluster strategy for [[categorical variable|categorical variables]] without the need to convert to numerical, which might introduce bias and innaccuracies

>[!warning] disadvantages
>- May lead to locally optimal solutions
>- Dependent on the initial modes (initial parameters)



