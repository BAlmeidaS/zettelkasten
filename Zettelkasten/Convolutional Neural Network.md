---
tags:
  - deep-learning
aliases:
  - CNN
---
*Convolution Neural Network* or *CNN* are a type of [[Neural networks]] architecture

The idea is to recognise *spatial patterns* on *input signals*, by striding a small *filter* or *kernel* through the input.

![[Pasted image 20240717144520.png]]

Each input for a CNN layers, related to image processing, has 3 parameters:
$\displaystyle \large height \times width \times channels$

*Channels* are the amount of "layers" that *feature map has*:
- For the first layer, if the image is grayscale, there will be 1 channel
- For the first layer, if the image is rgb, there will be 3 channel
- For the middle layers, the feature map will have the number of channels of the number of [[Filter - CNN|filters]] trained on the last layer

There are three main concepts:
- [[Filter - CNN]]
- [[Pooling - CNN]]

>[!note]
>The *first Convolution layers* identify simpler patterns (such as edges), whereas the *last Convolution layer* end up identifying more complex patterns
> 