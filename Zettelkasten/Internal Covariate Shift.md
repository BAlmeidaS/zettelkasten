---
tags:
  - deep-learning
---
Similar to [[Covariate Shift]] but it occurs within *deep neural networks* during training.

As the *parameters of the network are adjusted, the distribution of inputs to each layer can shift, leading to instability in the training process*. This can slow down the convergence of the network and make it more difficult to train effectively.

>[!hint] Still ongoing research
>While batch normalization was introduced partly to mitigate what was believed to be the effects of internal covariate shift, the concept itself and its exact implications are still areas of ongoing research and debate within the machine learning community.
>
>Some studies have suggested that internal covariate shift might not be as significant a problem as initially thought, and that other factors such as the choice of optimization algorithm or the architecture of the network may play larger roles in the challenges encountered during training deep neural networks.
>
>So, while internal covariate shift is a concept that has been proposed to explain certain difficulties in training deep neural networks, its precise impact and the best methods for addressing it are still subjects of active investigation and discussion.

