---
tags:
  - Russel-n-Norvig-chap-3
---
- state
- action
- [[Goal test]]
- [[Action Cost function]] / path cost

We have a initial state, and a solution is a path to the goal state. Each step we run a goal test to check if the algorithm finished. From each state there are several action that can be taken and they will lead to other states.

A solution of a search problem is a fixed sequence of actions.

A performance can be measured in four ways:
- [[Completeness]]
- [[Cost optimality]]
- [[Time complexity]]
- [[Space complexity]]

In order to compute time and space complexity, search problems on AI tend to work with [[Implicit graphs]] rather than [[explicit graphs]]
