---
tags:
  - paper
  - rate-35
---
URL: https://arxiv.org/pdf/2306.01323
Review: https://openreview.net/forum?id=oef30oScVB
Review average (1-5): 3.5
Conf: NeurIPS 2023

---

This paper focuses on the performance disparity on homophily and heterophily nodes in node-level classification tasks. It claims that although GNNs have good performance on both pure homophily and pure heterophily graphs, GNNs cannot perform well when dealing with graphs with both these two types of nodes. The paper then analyses the reason for different impact on majority and minority nodes and illustrates the aggregation function's contribution on this. It delves into the theoretical analysis, deriving a non-i.i.d PAC-Bayesian generalization bound based on the Subgroup Generalization bound of Deterministic Classifier. The theoretical analysis indicates that test nodes with larger aggregated feature distances and homophily ratio differences from training nodes experience performance degradation. The practical implications of the findings are demonstrated on real-world datasets.