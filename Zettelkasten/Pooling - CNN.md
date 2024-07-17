---
tags:
  - deep-learning
---
*Pooling* is a strategy applied to *reduce the size of the feature map*.
As a [[Filter - CNN]], it is defined by:
- *dimensions*
- [[Filter - CNN|stride]]
- [[Filter - CNN|padding]]

And a type of operation to reduce, like [[Average]] (AvgPoll) or *Maximum* (MaxPoll). This operation will be used to reduce the number on the filter to one final number.
![[average-pooling-a.gif|300]]
![[max-pooling-a.gif|300]]

**Polling layers have no learnable parameters**