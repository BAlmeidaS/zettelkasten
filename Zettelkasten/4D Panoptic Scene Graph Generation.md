---
tags:
  - paper
  - rate-35
  - year-2023
---
URL: https://arxiv.org/pdf/2405.10305
Review: https://openreview.net/forum?id=GRHZiTbDDI
Review average (1-5): 3.5
Conf: NeurIPS 2023

---

This is essentially a computer vision paper, although the temporal domain caught my attention.

This paper offers a novel perspective on understanding a 4D environment via the introduction of 4D Panoptic Scene Graph (PSG-4D). PSG-4D transforms 4D sensory data into nodes, representing entities with precise location and status data, and edges that capture temporal relationships. The authors have developed a high-quality PSG-4D dataset, which includes 3K RGB-D videos with a total of one million frames. Each frame comes with 4D panoptic segmentation masks and detailed, dynamic scene graphs. In order to solve PSG-4D, they propose PSG4DFormer, a model capable of predicting panoptic segmentation masks, tracking masks across the time axis, and generating corresponding scene graphs via a relation component. Extensive experiments demonstrate that their method forms a robust baseline for PSG-4D. Furthermore, the paper provides a real-world application example demonstrating how dynamic scene understanding can be achieved by incorporating a large language model into the PSG-4D system.