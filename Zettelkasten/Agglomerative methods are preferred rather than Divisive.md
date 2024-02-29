---
tags:
  - machine-learning
---
In [[Hierarchical clustering]], typically we opt for *agglomerative approaches* due to some facts:
- Simplicity and Intuitiveness
- Efficiency and Implementation
	*divisive algorithms* run dividing clusters into two, this is a common [[NP-hard]] problem, called [[optimal partition problem]] that has $\displaystyle \large O(2^{n})$ complexity, being $\displaystyle \large n$ the number of data points.

Though, this *does not mean that divisive approaches are useless*, especially when:
- we have large, well-separated clusters
- Theoretical considerations to create new insights 