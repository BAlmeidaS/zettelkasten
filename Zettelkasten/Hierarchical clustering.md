---
tags:
  - machine-learning
---
*Hierarchical clustering* creates a tree of clusters called a [[dendogram]], which represents the relationships among the data points.

**It does not require specifying the number of clusters in advance**.

- Does not require a predefined number of clusters.
- Can be *computationally expensive*, especially for large datasets.
- Provides a detailed dendrogram, offering insight into the data structure.

>[!note] How it does
>It can be approached in two ways: 
>1. *Agglomerative* (bottom-up) where each data point starts as a single cluster and pairs of clusters are merged as one moves up the hierarchy
>2. *Divisive* (top-down) where all data points start in one cluster which is interactively split as one moves down the hierarchy.
