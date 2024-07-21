---
tags:
  - deep-learning
---
Deep learning model to solve [[Semantic Segmentation]].

The idea is creating a network that builds many channels in its middle, like most of the [[Convolutional Neural Network|CNNs]], but towards the end it becomes more flat again, in order to *rebuild the initial image but with the labels per pixels*
![[Pasted image 20240721143919.png]]

In order to make the output bigger with less channels we use [[Transpose Convolution]].

Also it makes use of [[Residual Block|skip connection]] between layers of the same size, in order to all the "reconstruction layers" having the *low level features from early layers and the high levels from the middle one*.

![[Pasted image 20240721145541.png]]

The final arquitecture
![[Pasted image 20240721145617.png]]
* On the right of the U, the *light blue* comes from the [[Transpose Convolution]] while the *dark blue* comes from the left side.
* The last Conv (pink $\displaystyle \large 1 \times 1$) builds the final image with the channels equal to the number of classes of pixels
* The input is $\displaystyle \large h \times w \times 3$
* The output is $\displaystyle \large h \times w \times n_{classes}$

