---
tags:
  - paper
  - rate-4
  - year-2023
---
URL: 
Review: https://openreview.net/forum?id=RSGNGiB1q4
Review average (1-5): 4
Conf: NeurIPS 2023 Oral

---

The paper introduces an innovative perspective on knowledge graph embedding (KGE) models, allowing for generative model construction through maximum likelihood estimation (MLE). The incorporation of logical constraints enhances inference validity. The paper's clarity, well-structured presentation, and reimagining of training objectives as MLE have been mentioned as its strengths. The well-designed experiments further support the proposed methods. All reviewers are positive to very positive about his submission. I strongly recommend accepting this paper, as it significantly contributes a fresh perspective to the evolving landscape of KGE research

Additional: Knowledge graph (KG) is a different structure then Graph Neural Network (GNN). Both are indeed graphs but where KG differs is that it is not a Machine learning (ML) model, its just a way to "represent" relation between entities using an edge (predicate) while GNN is ML model that it learns the structure of the graph (neighbors and neighbor of neighbors) while training. This is why KG embedding is shallow in a sense that it could be merely an embedding of nodes obtained from either word embeddings such as [Word2Vec](https://en.wikipedia.org/wiki/Word_embedding) or other methods such as [TransE](https://proceedings.neurips.cc/paper/2013/file/1cecc7a77928ca8133fa24680a88d2f9-Paper.pdf), not accounting much for multi-hop context. Whereas GNN is indeed aimed at learning/encoding multi-hop context such as information about neighbors and neighbor of neighbors, into node embeddings, hence they are more rigorous then KG embeddings.


