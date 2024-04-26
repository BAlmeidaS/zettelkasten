---
tags:
  - deep-learning
---
*Batch normalisation* is a technique introduced to address [[Internal Covariate Shift]].

Batch normalisation helps stabilise the distribution of inputs to each layer by normalising the activations within mini-batches during training, which can lead to faster and more stable training of deep neural networks.

It smooths [[Cost function]] and speeds up learning.

![[Pasted image 20240426172114.png|600]]

Batch normalisation, *normalises the output of a layer across the mini-batch*.