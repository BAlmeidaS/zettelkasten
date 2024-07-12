---
tags:
  - deep-learning
aliases:
  - debias word embeddings
---
Word embeddings can carry ethical biases as emphasised by Bulukbasi et al. 2016 (Man is to Computer Programmer as Woman is to Homemaker? Debiasing Word Embeddings).

They propose a technique to *debias word embeddings*

1. Identify bias direction on the embedding
2. Neutralise the bias: For every word that is not definitational, project to *unbias axis* to get rid of bias
3. Equalise pairs - Guarantee that every biased word (boy and girl, for instance) are equidistant to the unbias axis

As an example this would be the embedding of some words, and the bias direction (in this example gender) and the unbias direction

![[Pasted image 20240712184034.png|500]]

step 2 - neutralise bias (remove from doctor and babysitter some type of gender bias):
![[Pasted image 20240712184115.png|300]]
![[Pasted image 20240712211336.png|700]]

step 3 - equalise (make grandmother and grandfather equidistant to babysitter)
![[Pasted image 20240712184219.png]]
![[Pasted image 20240712212033.png|700]]

