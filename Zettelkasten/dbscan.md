---
tags:
  - machine-learning
---
*Dbscan* or *Density-Based spatial Clustering of Applications with Noise*, is a [[Partitional clustering]].

It is a simple algorithm that:
- *does not need to specify number of cluster*
- *Handles well noise/outliers*
- Can find *non-linearly separable clusters* (arbitrary shaped clusters)
- finds the clusters by itself, isolating high-density regions from low-density.

![[Pasted image 20240229202646.png]]

It has 2 [[Hyperparameters of the model|Hyperparameters]]:
- $\displaystyle \Large \epsilon$ :  max distance between two samples
- $\displaystyle \large N_{min}$ : Number of samples in a neighbourhood to a point be considered as a *core point*
![[Pasted image 20240229202353.png|400]]

Points are defined as *core points*, *border points* and *outliers*
![[Pasted image 20240229202552.png|400]]

>[!note] algorithm
>1. The algorithm starts with an arbitrary starting point that has not been visited. It explores the neighbourhood of this point using $\displaystyle \large \epsilon$ and $\displaystyle \large N_{min}$ to determine if it forms a cluster.
>2. If the point has sufficiently many points in its ε-neighborhood, it starts a cluster. Otherwise, it marks the point as noise (later, this noise could become part of a cluster).
>3. For a point found to be part of a cluster, it expands the cluster by exploring its neighbours, thus growing the cluster iteratively.
>4. The process repeats until all points have been processed.
