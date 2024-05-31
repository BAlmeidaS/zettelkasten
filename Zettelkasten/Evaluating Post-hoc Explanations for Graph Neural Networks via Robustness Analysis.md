---
tags:
  - paper
  - rate-4
  - year-2023
---
URL: 
Review: https://openreview.net/forum?id=eD534mPhAg
Review average (1-5): 4
Conf: NeurIPS 2023 Oral

---

Among all strengths that reviewers mentioned, this paper is particularly well motivated and focuses on a very important problem, tackling a gap between on evaluating the explanation for GNN. The detailed discussion on the drawbacks of different evaluation protocols is also appreciated. The experimental study is solid, with user study and diverse criteria.

This paper studies the explainability evaluation of GNNs, and proposes a new evaluation paradigm. Inspired by adversarial robustness, it uses a generative model (VGAE) to fulfill the explanation subgraph, randomly perturbs the fulfilled parts, and uses the OOD scores of perturbed graphs to measure the importance of explanation subgraph. Experiments are done on several datasets and show the improved evaluation quality w.r.t. diverse criteria.