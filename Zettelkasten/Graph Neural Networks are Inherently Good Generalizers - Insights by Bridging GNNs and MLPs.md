---
tags:
  - paper
  - rate-3
---
URL:
Review: https://openreview.net/forum?id=dqnNW2omZL6
Review average (1-5): 3
Conf: ICLR 2023

---

This paper presents an efficient model, PMLP, which achieves the GNN-level generalization and accuracy at the cost of training an MLP (which is much cheaper than training a GNN). The key idea is to decouple the node's information processing from the message passing operations. In PMLP, the weight values of a GNN are trained in the MLP form, and then only at inference stage the message passing operations are introduced. By showing various empirical results, using PMLP and GNNs shows similar performance, and using PMLP is much more efficient than using GNNs. PMLPs even achieve better robustness than GNNs when introducing structural noise to the graph. Theoretical analysis is also presented by analyzing the neural tangent kernels of MLP, PMLP and GNN. It is shown that the message passing operation makes PMLPs and GNNs generalize differently from MLPs on out-of-distribution test data: while all models degrade to linear extrapolation on OOD data, PMLPs and GNNs have their linear coefficients depend on the node degree to preserve more information from the data. The reviewers pointed to the gap to explain why PMLPs achieve performance close to GNNs, a realistic graph OOD scenario, differentiation with APPNP. The authors did a good job in responding to reviewers’ comments, leading to increased scores and an overall positive assessment from reviewers.