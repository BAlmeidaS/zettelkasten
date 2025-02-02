---
tags:
  - machine-learning
---
A model with **low bias** typically has **high variance** (complex models like deep neural networks).

A model with **low variance** typically has **high bias** (simpler models like linear regression).

The goal is to find a **balance**: a model that captures the true patterns in the data (low enough bias) while also being generalisable to new data (low enough variance)

#### how to control the trade-off?

**Increase complexity (reduce bias, increase variance)**: Use deeper models, more parameters, more flexible algorithms.

**Reduce complexity (increase bias, reduce variance)**: Use regularisation ([[L1 Regularisation|L1]] or [[L2 Regularisation|L2]]), fewer parameters, simpler models.

**Use more data**: More training data can help high-variance models generalise better.

[[cross validation]] helps detect overfitting, thus, finding the sweet spot.