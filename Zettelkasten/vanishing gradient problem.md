---
tags:
  - deep-learning
aliases: []
---
A common problem on deep learning, occurs when [[gradient]] becomes very small as they are propagated back through the network during [[back-propagation]].

*This makes difficult for the lower layers learn effectively*, leading to slow or stalled learning.

Two noticeable functions that have this problem are [[Sigmoid function]] and [[Hyperbolic Tangent function|tanh]].

---
see also [[exploding gradient problem]]