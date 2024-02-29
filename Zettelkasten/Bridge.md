---
tags:
  - machine-learning
---
Bridge is a [[hard clustering]] that combines the [[k-means]] and [[dbscan]].

The idea is to perform a *k-means* to partition the dataset in k-clusters, then run a *dbscan* to remove outliers and noise from this dense regions, and a last *k-means* runs to fine tune the centroids.