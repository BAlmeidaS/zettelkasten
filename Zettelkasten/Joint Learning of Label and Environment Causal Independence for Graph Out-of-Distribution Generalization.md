---
tags:
  - paper
  - rate-3
---
URL: https://arxiv.org/abs/2306.01103
Review: https://openreview.net/forum?id=z3HACY5CMa
Review average (1-5): 3
Conf: NeurIPS 2023

---

This paper proposes a new graph learning model to incorporate label and environment causal independence (LECI) for solving the graph OOD generalization problem. The authors first introduce two causal independence properties to distinguish causal and spurious subgraphs. Enforcing environment causal independence properties and utilizing the environment label information, LECI is able to identify causal subgraphs for invariant predictions. The authors further leverage an adversarial learning strategy to learn the label and environment casual independence. In contrast to the previous graph OOD methods which commonly assume non-existence of the environment information, LECI instead fully utilizes environment information and introduces a graph-specific environmental exploitation algorithm. Extensive experiments on GOOD and DrugOOD benchmark datasets demonstrate the superiority of LECI among other baseline methods.