---
tags:
  - Python
---
How numpy treats operations with arrays with different shape: https://numpy.org/doc/stable/user/basics.broadcasting.html

>[!tip] code example
>```python
>from numpy import array, argmin, sqrt, sum
>observation = array([111.0, 188.0])
>codes = array([[102.0, 203.0],
>                [132.0, 193.0],
>                [45.0, 155.0],
>                [57.0, 173.0]])
>diff = codes - observation    # the broadcast happens HERE!
>dist = sqrt(sum(diff**2,axis=-1))
>argmin(dist)
>```
>![[Pasted image 20240612171124.png]]

