---
tags:
  - machine-learning
---
An strategy to evaluate [[Random Walk Embedding|random walks]] in a graph.

*Node2Vec* extends the idea of [[by introducing two hyperparameters, ppp and qqq, which control the depth and breadth of the walks.

- **ppp**: Return parameter. This parameter controls the likelihood of immediately revisiting a node in the walk. A higher ppp value means the walk is less likely to go back to the previous node, encouraging exploration.
- **qqq**: In-out parameter. This parameter allows the walk to switch between breadth-first search (BFS) and depth-first search (DFS) strategies. A higher qqq value biases the walk towards BFS (exploring neighbours of the current node), while a lower qqq value biases it towards DFS (exploring the network deeply).