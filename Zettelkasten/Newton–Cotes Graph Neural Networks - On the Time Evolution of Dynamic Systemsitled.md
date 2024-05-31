---
tags:
  - paper
  - rate-35
---
URL: 
Review: https://openreview.net/forum?id=CnvZ7FIyAD
Review average (1-5): 3.5
Conf: NeurIPS 2023 spotlight

---

This paper builds on recent advances in deep learning for physical simulation to produce reliable results of long-term consecutive predictions. The authors provide a proof that equivariant graph neural networks learn a linear map from initial velocity to a target velocity, and propose to inject inductive bias based on Newton-Cotes (NC) formulas as alternative of standard equivariant graph convolution. The paper introduces techniques for training, such as a new objective and a new regularization loss for higher order features, and also gives theoretical guarantee that variance can be reduced by increasing the degree of NC formula. Experiments in various multiple body interaction systems demonstrate that the proposed model outperforms state-of-the-art baselines .