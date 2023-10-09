A special kind of [[List]] 

A "stack" that pops the node with the minimum cost according to some evaluation function $f$

Usually it is implemented with [[HEAP]] to be cost efficient

| function | complexity |
| -------- | ---------- |
| Add      | $\Large O(\ log(n)\ )$ |
| Remove   | $\Large O(\ log(n)\ )$ |