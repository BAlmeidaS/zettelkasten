---
tags:
  - deep-learning
---
Algorithm to solve [[Object Detection]].

The Idea is creating multiple *windows* and *sliding* them through the image and do like a [[Image Classification with localisation]] on those windows.
![[Pasted image 20240719212923.png|500]]

The way to implement this using [[Convolutional Neural Network|CNNs]] **in an efficient way** is relying on the fact that a *fully connected layer might be transformed to a convolutional layer*:

For instance the following architecture:
![[Pasted image 20240719214142.png]]

Might be changed to:
![[Pasted image 20240719214852.png]]

And they mean *the same thing*, FC on the second image is a *CNN layer* with the number of filters with the same size of the last layer, so the final dimension is $\displaystyle \large 1\times 1\times n$, the final layer ([[softmax function|softmax]]) is the same, the 4 numbers are on the this tensor not on the flatted version.

*The advantage of this approach is to be able to compute multiple sliding windows at once*

>[!example]
>let's say that the sliding window is $\displaystyle \large 14\times 14 \times 3$ (as the image above), and we want to slide this windows over an image that is $\displaystyle \large 28\times 28\times 3$, instead of making multiple prediction using the network above (on "slices" of the image), we can *run one unique prediction* and interpret the results.
>
>Using the network above, and this bigger image, this are the results:
>![[Pasted image 20240719215627.png]]
>
>The final layer is, because of the bigger input, $\displaystyle \large 8 \times 8 \times 4$, being each cell $\displaystyle \large 1 \times 1 \times 4$ the softmax resultant of each one of the $\displaystyle \large 14\times 14\times 3$ sliding windows that passed through the image ($\displaystyle \large 8 * 8 = 64$):
>![[Pasted image 20240719220020.png]]

The problem here is that, it assumes that the bounding box are *very accurate positioned* and they are squares.
