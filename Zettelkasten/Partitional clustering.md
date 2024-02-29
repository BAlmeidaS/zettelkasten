---
tags:
  - machine-learning
---
*Partitional clustering* is a type of [[hard clustering]] without any hierarchical structure.

**number of clusters is specified a priori**

- Fixed number of clusters.
- Tends to be *faster and more scalable* to large datasets.
- Sensitivity to the initial partition and the presence of outliers.

>[!note] How it does
>The method is typically starting with an initial partitioning and then interactively relocates data points to improve the partitioning based on a specific criterion.

Examples are [[k-means]] and [[dbscan]]