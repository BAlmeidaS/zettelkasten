---
tags:
  - deep-learning
aliases:
  - IoU
---
*Intersection Over Union* is a *metric* to measure how good a *bounding box* from [[Object Detection]] fit with the original label:
![[Pasted image 20240720205544.png|200]]

Basically we will measure how much the intersection of the areas is based on the total area
![[Pasted image 20240720205729.png|350]]

Usually, $\displaystyle \large IoU \ge 0.5$ is conventionally set as "correct" .