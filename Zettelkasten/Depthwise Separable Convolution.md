---
tags:
  - deep-learning
aliases:
  - mobilenet
---
Similar to [[Convolutional Neural Network|Convolutions]] but in a way that the *number of multiplications made is reduced*.

>[!info] the original filter of CNN
>the original filter of CNNs are like this. 
>![[Pasted image 20240718135814.png|500]]

The *Depthwise Separable Convolution* is divided into two:
### Depthwise Convolution

The Idea is having a different [[Filter - CNN|filter]] (so, different weights) *for each input channel* (rather than applying through all the channels).

![[Pasted image 20240718135735.png]]
so the output will have *the same number of channels as the input*.

### Pointwise Convolution

At this step the number of channels will be increased using [[Convolution of 1x1 filter]]
![[Pasted image 20240718140058.png]]

>[!note] The difference of the number of multiplications
>Considering the *normal convolution* vs *depthwise + pointwise convolution* with the case presented above, input $\displaystyle \large 8\times8\times3$  and output $\displaystyle \large 8\times8\times256$
>
>normal convolution number of multiplications:
>$$\displaystyle \Huge \begin{eqnarray} 
>5*5*3*256*(8*8) = 1,228,800
>\end{eqnarray}$$
>$\displaystyle \large (8*8)$ is the numbers of [[Filter - CNN|stride]] of the filter of the feature map
>
>while with depthwise separable convolutions:
>$$\displaystyle \Huge \begin{eqnarray} 
>depthwise &=& 5*5*3*(8*8) \\
>&=& 4800
>\\[8pt]
>pointwise &=& 1*1*3*256*(8*8)\\
>&=& 49152
>\\[8pt]
>final &=& depthwise + pointwise \\
>&=& 54,312
>\end{eqnarray}$$
>The factor is:
>$$\displaystyle \Huge \begin{eqnarray} 
>factor &=& \dfrac{54,312}{1,228,800} \approx 0.044\\
>\end{eqnarray}$$


The factor that *depthwise separable convolution* reduce is:
$$\displaystyle \Huge \begin{eqnarray} 
factor \approx 
\dfrac{1}{n_{out}} + \dfrac{1}{f^2}
\end{eqnarray}$$

