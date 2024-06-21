---
tags:
  - deep-learning
aliases:
  - GNN
---
Machine Learning in Graphs might be defined into 3 main types:
- [[Node-level Task - Traditional ML methods]]
- [[Edge-level Task - Traditional ML methods]]
- [[Graph-level Task - Traditional ML methods]]

The problem with the traditional methods is that they demand a lot of hand-craft feature engineer. [[Representation Learning]] is the act of building such features automatically and they can be expanded here with the concepts of [[embedding]], or more specifically [[Node Embeddings]]




The idea behind GNN is removing the [[Feature Engineering]] mandatory to use *graph structures* on machine learning models. This is what is known as [[Representation Learning]], the act of building the features automatically.

For instance considering the a node representation, the idea is *learning a function that maps a node to a vector of Reals*:
Given a node $\displaystyle \large u$, find a function $\displaystyle \large f: u \rightarrow \mathbb{R}^d$. This vector $\displaystyle \large \mathbb{R}^d$ is an [[embedding]].

[[Deep walk]] is one of the first embedding created using GNNs. More details in [[Node Embeddings]]


---

![[Pasted image 20240620131936.png|400]]
![[Pasted image 20240620175356.png|400]]

