---
tags:
  - deep-learning
aliases:
  - skip connection
---
The main goal of *Residual Blocks* are to avoid [[vanishing gradient problem]] that deep [[Convolutional Neural Network|CNNs]] have. *ResNet* is a famous network to implement it massively.

The idea is to create a connection between a previous information on the network with a later information, and "connection" is called *skip connection*