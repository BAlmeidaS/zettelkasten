---
tags:
  - machine-learning
---
*K-medoids* is a [[Partitional clustering]], more specifically a [[centre-based clustering]].

It is an extension of [[k-means]], but with some significant differences.

K-medoids use the concept of *medoids*, instead of centroids. *Medoids are actual data points that play the role of the centre*.

Because medoids are actual data points, k-medoids is *less sensitive to outliers and noise*. However, for the same reason, it is *more computationally intensive*.

It pairs well with any [[distance function]] and is commonly used when the dataset has many outliers.
