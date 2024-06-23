---
tags:
  - machine-learning
---
An strategy to evaluate [[Random Walk Embedding|random walks]] in a graph.

*Node2Vec* extends the idea of [[Deep Walk]] by introducing two hyperparameters, $\displaystyle \large p$ and $\displaystyle \large q$, which control the amount of "[[Depth-first search|DFS]]" and "[[Sequential Backward Selection|BFS]]" that the walk will do

- $\displaystyle \large p$ : Return parameter. This parameter controls the likelihood of immediately revisiting a node in the walk. A higher $\displaystyle \large p$ value means the walk is less likely to go back to the previous node, encouraging exploration.
- $\displaystyle \large q$ : In-out parameter. This parameter allows the walk to switch between breadth-first search (BFS) and depth-first search (DFS) strategies. A higher $\displaystyle \large q$ value biases the walk towards BFS (exploring neighbours of the current node), while a lower $\displaystyle \large q$ value biases it towards DFS (exploring the network deeply).

