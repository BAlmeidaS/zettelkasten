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
>![[Pasted image 20240722170154.png]]

The number of *learnable parameters* on a CNN layer is:
$$\displaystyle \Huge \begin{eqnarray} 
\#params &=& 
filter_{height} * filter_{width} * filter_{channel} + Bias_{one\ per\ filter}
\end{eqnarray}$$

**Polling layers have no learnable parameters**

The *output feature map* of a *CNN* layer is defined as:
$$\displaystyle \Huge \begin{eqnarray} 
output\ dimmensions =\ &(&
\left\lfloor\dfrac{input_x + 2*padding_x - filter_x}{stride_x}\right\rfloor,
\\&&
\left\lfloor\dfrac{input_y + 2*padding_y - filter_y}{stride_y}\right\rfloor,
\\&&
\#\text{filters}
)
\end{eqnarray}$$

