---
tags:
  - deep-learning
aliases:
  - YOLO
---
Algorithm to solve [[Object Detection]].

Similar to [[Sliding Window]] in the sense that the output will be a volume having in each cell the result of a [[softmax function|softmax]] for that box. The main difference here is that, *YOLO* will divide the image into a grid (3x3 let's say) and will apply [[Image Classification with localisation]] in that cell - so being a 3x3 grid the output will be $\displaystyle \large 3\times 3 \times n$. In practice this grid is way bigger (like 19x19)

Again, $\displaystyle \large n$ will be composed of $\displaystyle \large P_c, b_x, b_y, b_h, b_w, c$
- $\displaystyle \large P_c$: have (1) or not (0) something on the image
- $\displaystyle \large b_x$: position of the centre of the bounding box on the x-axis
- $\displaystyle \large b_y$: position of the centre of the bounding box on the y-axis
- $\displaystyle \large b_h$: height of the bounding box
- $\displaystyle \large b_w$: width of the bounding box
- $\displaystyle \large c$: class of the object identified

![[Pasted image 20240720204236.png|300]]

*The objects belong to the cells that contains their **central point/middle point***.

Also, the $\displaystyle \large b$ variables, they are relative to the *inner cell*, not to the global image. Which means that two different cells might have an object on the position $\displaystyle \large 0,0$ (for instance). And it might go *outside* the cell, as the following example:
![[Pasted image 20240720205231.png|300]]

