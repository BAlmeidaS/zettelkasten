---
tags:
  - machine-learning
---
An strategy to evaluate [[Random Walk Embedding|random walks]] in a graph.

*DeepWalk* performs a series of truncated *random walks starting from each node in the graph*.

These walks are akin to simple random walks where, at *each step, the next node is chosen uniformly at random from the current node's neighbours*.

The sequences generated from these random walks are then used on [[Random Walk Embedding]] by treating the sequences as sentences and applying the [[Skip-gram]] model, similar to how [[word2vec]] works for natural language.


---

https://arxiv.org/abs/1403.6652