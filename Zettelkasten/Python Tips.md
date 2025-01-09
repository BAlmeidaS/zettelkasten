---
tags:
  - computer-languages
---
### Interaction in notebooks
Interact is a nice [ipywidgets](https://ipywidgets.readthedocs.io/en/stable/) stuff to use on *notebooks*:
```python
# on a notebook try:
@interact(n=(0, 10))
def display_faces(n):
	print(n*2)
```
