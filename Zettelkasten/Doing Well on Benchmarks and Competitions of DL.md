---
tags:
  - deep-learning
aliases:
  - tips benchmarks
---
Some tips from Andrew Ng to perform well on benchmarks from [[Neural networks]], but not used on *production systems*:
1. *Ensembling*: Train several networks independently (each one with different initialisation numbers) and average their outputs
2. *Multi-crop* at test time: Run classifier on multiple versions of test data and average results!