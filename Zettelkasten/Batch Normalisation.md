---
tags:
  - deep-learning
---
*Batch normalisation* is a technique introduced to address [[Internal Covariate Shift]].

Batch normalisation helps stabilise the distribution of inputs to each layer by normalising the activations within mini-batches during training, which can lead to faster and more stable training of deep neural networks.

It smooths [[Cost function]] and speeds up learning.

![[Pasted image 20240426172114.png|600]]

Batch normalisation, *normalises the output of a layer across the mini-batch*.

![[Pasted image 20240426173311.png|600]]

So if you have a batch of 32, there will be 32 $\displaystyle \large \hat z^{[l]}_i$, so the mean ($\displaystyle \Large \mu_{z^{[l]}_i}$) is the mean of the batch for that z, and std dev ($\displaystyle \Large \sigma^2_{z^{[l]}_i}$) as well. So they are the ones calculated over these 32 values.

After normalising it ($\displaystyle \large \hat z$), this is *not* what goes to the [[activation function]] to compute $\displaystyle \large a$, instead, this goes to another function to define $\displaystyle \large y^{[l]}_i$, and this $\displaystyle \large y^{[l]}_i$ is what will be passed to the activation function. 

Pay attention that, *$\displaystyle \large \gamma$ and $\displaystyle \large \beta$ , are two trainable [[Parameters of the Model|Parameters]]*, thus will be learned on the training.

>[!important] During test?!
>During Test (or just to predict, not training), the mean and std dev used are the ones calculated over the *entire* training. Therefore, they will not move on predict.
>
> ![[Pasted image 20240426175908.png|450]]
