---
tags:
  - computer-science
---
[[single-link hierarchical clustering]] has in a poorly implementation [[Time complexity]] of $\displaystyle \large O(n^3)$ - each step that you connect you recalculate from the scratch all the distances again.

However, this performance can be improved to $\displaystyle \large O(n^2log(n))$ by using [[Minimum Spanning Tree]] and [[Kruskal's algorithm]]

...