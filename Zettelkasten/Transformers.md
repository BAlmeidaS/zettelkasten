---
tags:
  - deep-learning
---
*Transformers* are an evolution of [[Recurrent Neural Network|RNNs]] with a connection with [[Convolutional Neural Network|CNN]].

The architecture is based in two concepts:
- [[Self-Attention]]
- [[Multi-head Attention]]

Apart from that the arquitecture defines two blocks (an Encoder and a Decoder) and because it does not use any type of [[Recurrent Neural Network|RNN]] or [[Convolutional Neural Network|CNN]], it defines a *feature engineer* called *positional encoding*, to encode in each word the position on the sentence.

![[Pasted image 20240716192909.png|600]]