---
tags:
  - deep-learning
aliases:
  - padding
  - stride
  - cross-correlation
---
*Filters* in [[Convolutional Neural Network|CNN]], also known as *Kernels*, are the set of parameters that each layer of *CNN* will learn.

A layer of CNN defines:
1. the dimmensions of the filters: *Height and Weight*, which must be smaller than the *feature map* (signal). The filter has also the number of channels *C* as the number of *channels* from the *feature map* of the last layer.
2. The *number of filters* - In the image above, *K* are being generated.
![[Pasted image 20240717145530.png]]

3. *padding* - number of zeros filling the feature map on the borders
![[Pasted image 20240717150100.png]]

4. *stride* - number of pixels by which the filter will move after each operation
![[Pasted image 20240717150136.png]]


The filter will run *an [[element-wise multiplication|element-wise product]] with each set of numbers* that it will fit (based on padding and stride) and *a sum across all the results* (height, width, and channels)
![[convolution-layer-a.gif|500]]

One layer of *CNN* might contain multiple filters, each filter will generate a *new channel for the output*:
![[1_m4IsBwYv7QEND-y6xWw3Yw.gif|500]]

>[!note]
>The idea of *filters* is identifying pattern, *edges* and *patterns*

*Each filter has only one bias, regardless its size!*

>[!note] cross-correlation
>Rigorously, there is a flip that must be done (horizontally and vertically) on the filters, before applying it on the feature map. Without this flipping this *convolution* is better named as *cross-correlation*, but conventionally we call this operation *convolution* anyway.

