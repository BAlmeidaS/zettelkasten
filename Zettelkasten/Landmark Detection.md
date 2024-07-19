---
tags:
  - deep-learning
---
A type of problem that [[Convolutional Neural Network|CNNs]] are useful to solve.

Kind of an evolution of [[Image Classification with localisation]], the goal here is to recognise specific points on an image (like the corner of the eyes, the points the form a month).

For that, the network should output *as many points $\displaystyle \large x, y$ as we need*. Of course you need a *labelled dataset*.
![[Pasted image 20240719130058.png]]

The same can be extend to *poses* of a person (like bones)
![[Pasted image 20240719130033.png]]

Important to say that *landmarks must be consistent across all the images*, which means that, if landmark 37 is the tip of the nose, it must be the tip of the nose in all images.