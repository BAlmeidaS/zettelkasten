---
tags:
  - paper
  - rate-35
  - year-2023
---
URL: https://arxiv.org/abs/2309.13625
Review: https://openreview.net/forum?id=YmEDnMynuO
Review average (1-5): 3.5
Conf: NeurIPS 2023

---

In this paper, the authors present an adapter-style tuning method, termed as GraphAdapter, that explicitly captures the dual-modality structure knowledge by utilizing a dual knowledge graph, leading to enhanced adapter-style transfer learning. Specifically, the authors identify two key challenges in existing adapter-style approaches for efficient transfer learning, including the deficiency in modeling task-specific knowledge from only a single modality, and the neglect of explicitly exploiting the structural knowledge in downstream tasks. Motivated by these two limitations, the authors propose a novel tuning method for visual-language models that incorporates task-specific knowledge for downstream tasks through the integration of textual and visual structure knowledge, based on graph learning. In particular, the proposed method establishes a dual knowledge graph consisting of a textual knowledge subgraph and a visual knowledge subgraph. Consequently, the feature adapter can effectively leverage the inner-modality and cross-modality structure knowledge for superior tuning performance. Experiments on 11 benchmarks convincingly demonstrate the effectiveness of the proposed GraphAdapter approach.