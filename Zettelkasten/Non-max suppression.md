---
tags:
  - deep-learning
---
A technique used on [[Object Detection]] to *avoid that an object is detected multiple times*.

On predict time, a common prediction will be something like this:
![[Pasted image 20240720210233.png]]
*Non-max supression* will clean this prediction.

1. Basically it will get the higher prediction (in this example $\displaystyle \large 0.9$) and will remove all the other bounding boxes with high [[Intersection Over Union|IoU]] with that one will be removed. 
2. Then it goes to the remaining rectangles and get the maximum and do the same. Until you passed through all the bounding boxes.

