---
tags:
  - deep-learning
---
*t-SNE* is an unsupervised non-linear [[dimensionality reduction]] technique to visualise high-dimensional data.

The t-SNE algorithm finds the similarity measure between pairs of instances in higher and lower dimensional space. After that, it tries to optimise two similarity measures. It does all of that in three steps. 

1. t-SNE models a point being selected as a neighbour of another point in both higher and lower dimensions. It starts by calculating a pairwise similarity between all data points in the high-dimensional space using a Gaussian kernel. The points that are far apart have a lower probability of being picked than the points that are close together. 
2. Then, the algorithm tries to map higher dimensional data points onto lower dimensional space while preserving the pairwise similarities. 
3. It is achieved by minimising the divergence between the probability distribution of the original high-dimensional and lower-dimensional. The algorithm uses gradient descent to minimise the divergence. The lower-dimensional embedding is optimised to a stable state.