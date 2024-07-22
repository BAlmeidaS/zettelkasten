---
tags:
  - deep-learning
---
A Siamese Network is a type of [[Neural networks]] that consists of two or more identical sub-networks sharing the same parameters and weights.

These sub-networks process two different input vectors to produce output vectors.

The primary purpose of Siamese Networks is to determine the similarity between the input vectors by comparing their outputs. Useful to solve [[One Shot Learning]], they achieved good results on *DeepFace* to build *face recognition*
![[Pasted image 20240722141117.png]]

The Idea is measuring the [[Similarity function|similarity]] between $\displaystyle \large y_1$ and $\displaystyle \large y_2$ in order to say if this two people are the same, by getting the output vector of this [[Convolutional Neural Network|CNN]] and considered as an [[embedding]]