---
tags:
---
An [[Uninformed Search]] algorithm

The Idea is starting a search from the start and from the goal, and see when they touch each other. Usually you search in each side a [[Uninformed Search]], but you can start as well any [[Informed Search]] as well.

| Criterion | BFS |
| --------- | --- |
| [[Completeness]]? | Yes |
| [[Cost optimality]]? | Yes |
| [[Time complexity]] | $\displaystyle \Large O(b^\tfrac{d}{2})$ |
| [[Space complexity]] | $\Large O(b^\tfrac{d}{2})$ |
$\large b$ is the [[branching factor]]
$\large d$ is the depth of the shallowest solution

![[Pasted image 20231009022312.png]]

![[Pasted image 20231009022720.png]]

---
last update: 09-10-2023
