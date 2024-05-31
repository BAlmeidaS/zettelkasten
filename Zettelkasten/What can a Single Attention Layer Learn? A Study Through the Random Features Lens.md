---
tags:
  - paper
  - rate-no
---
URL: 
Review: https://openreview.net/forum?id=wX8GuzDSJR
Review average (1-5): 3
Conf: NeurIPS 2023

---

This paper explores what a single attention layer learns through random feature analysis. The analysis provides valuable insights and is of interest to the community. The paper has received generally positive reviews from the reviewers, and the rebuttal has addressed most of the concerns. One remaining issue is the use of ReLU instead of softmax. I understand that this choice is primarily driven by the challenges in analyzing the softmax function in a general context, and the authors have referenced a study <73> suggesting that ReLU could be comparable to softmax (although this comparison has yet to be validated across a wider range of models and datasets). One potential improvement, as also highlighted by one of the reviewers, is to conduct softmax experiments within the paper's simulated environment and gather additional data points to support the claim.

<73> A Study on ReLU and Softmax in Transformer

---

This paper uses a "technique" used on [[MLP-Mixer - An all-MLP Architecture for Vision]], to summarise the temporal link information on *link-encoder*. Although this is good, the MLP-mixer was criticised to be data-hungry and parameter-inneficient. *Maybe  the model could achieve even better results with Convolutions to information summarising.*

21
