---
tags:
  - deep-learning
---
The idea of *anchor boxes* is to have some type of "common shapes" that the predictions are attached to those *anchor boxes*, and the idea is that it might be more likely to be correct the prediction.

*Each object in training image is assigned to grid cell that contains object's midpoint and to an anchor box for the grid cell with the highest [[Intersection Over Union|IoU]]*.

So each object is defined as a pair, *grid cell* and *anchor box*. And this is a way to coexist different objects one over the other.

*Also, Anchor Boxes helps the model to specialise faster and better*.

>[!example]
>![[Pasted image 20240720212641.png|500]]
>
>In this example, pedestrian should be attached to *anchor box one* while the car must be attached to the *anchor box 2*.

Some *automatic way* to define the anchor boxes are by using [[k-mea]]