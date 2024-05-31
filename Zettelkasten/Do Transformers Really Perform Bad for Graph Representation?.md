---
tags:
  - paper
  - rate-35
  - year-2021
aliases:
  - GraphFormer
---
URL: https://arxiv.org/pdf/2106.05234
Review: https://openreview.net/forum?id=OeWooOxFwDa
Review average (1-5): 3.5
Conf: NeurIPS 2021

---

We have explored the direct application of Transformers to graph representation. With three simple, yet effective graph structural encodings, the proposed GraphFormer works surprisingly well on a wide range of popular benchmark datasets.

The paper proposed a simple Transformer-based neural network architecture for graph data, called GraphFormer. Inspired by the positional encoding in NLP, GraphFormer encodes the structural information of the graph into the Transformer architecture via 1) centrality encoding, which incorporates degree information in computing the node embeddings, 2) spatial and edge encoding, which utilizes the shortest path between nodes to determine the edge biases in self-attention. In addition, the author added a set of virtual nodes to GraphFormer that connects to all nodes via "virtual" edges. The author compared GraphFormer with other models in several molecule/chemistry graph classification tasks and show that GraphFormer significantly outperforms the other methods, including several SOTA Message-Passing Graph Neural Network (MPGNN) models.