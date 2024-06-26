---
tags:
  - paper
  - rate-35
  - year-2023
  - reviewed
---
URL: 
Review: https://openreview.net/forum?id=ayPPc0SyLv1
Review average (1-5): 3.5
Conf: ICLR 2023

---
In this paper, they carefully design and propose the GraphMixer network for temporal link prediction in dynamic graphs. With a carefully designed and ablate architecture separated into three components, the link-encoder, node-encoder, and MLP-Mixer based link classifier, they are able to achieve high performance on this task that has only previously been attained with RNN and Self-Attention based architectures. They include extensive experiments to study the different architecture choices they made and their effect on performance and generalization.

---

The authors present a simple and elegant solution that achieves state-of-the-art performance on temporal graph learning-related tasks. The proposed solution has the potential to open the door to research for simpler, more interpretable, yet effective solutions.

The result relies a lot on which feature use for each dataset, they even purpose this as a future contribution to the area.

There solution is based on [[MLP-Mixer - An all-MLP Architecture for Vision]], although they say that it could be done using [[Graph Attention Networks|GAT]], and they prove on Figure 7. But they decide to keep with the MLP-mixer due to its simplicity.

