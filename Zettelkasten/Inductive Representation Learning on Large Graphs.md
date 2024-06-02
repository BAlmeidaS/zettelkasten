---
tags:
  - paper
  - rate-no
---
URL: https://arxiv.org/abs/1706.02216
Review: -
Review average (1-5):
Conf: NeurIPS 2017

---

The paper titled "Inductive Representation Learning on Large Graphs" introduces GraphSAGE, a framework designed to generate low-dimensional node embeddings in an inductive manner, allowing for the inclusion of previously unseen nodes and graphs during inference. Traditional embedding methods are typically transductive, requiring all nodes to be present during training, which limits their application in dynamic, real-world scenarios. GraphSAGE overcomes this by learning a function that samples and aggregates features from a node's local neighborhood, thereby creating embeddings based on node attributes and their structural context. The approach was tested on several benchmarks, including citation networks, Reddit post classifications, and protein-protein interaction graphs, demonstrating superior performance over existing methods and strong generalization capabilities to new data.

---

The first paper to use Message Passing Neural Networks (MPNNs) to predict edges on graphs using Graph Neural Networks (GNNs) is "Inductive Representation Learning on Large Graphs" by Will Hamilton, Zhitao Ying, and Jure Leskovec, published in 2017. This paper introduces the GraphSAGE algorithm, which performs inductive learning on large graphs and includes tasks such as node classification, link prediction (which involves predicting edges), and clustering.

GraphSAGE is a significant contribution to the field of graph representation learning as it allows for inductive learning, meaning it can generate embeddings for nodes that were not seen during training. This ability is crucial for tasks involving dynamic graphs where new nodes and edges continually appear.