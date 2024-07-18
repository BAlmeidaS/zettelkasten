---
tags:
  - deep-learning
aliases:
  - network in network
  - bottleneck layer
---
A $\displaystyle \large 1 \times 1$ [[Filter - CNN]] connects the whole numbers through the channels and apply some *non regularity*

![[Pasted image 20240717203705.png]]

You can use this to *shrink* the number of channels, as a *pooling does to the width and height*
![[Pasted image 20240717203836.png|500]]

This *shrink* can be used to create *bottleneck layer* on [[Convolutional Neural Network|CNNs]] to *reduce the number of parameters*:
![[Pasted image 20240718120640.png|700]]

---

Of course, the number of channels might be the same or even increase.