---
aliases:
  - "202401311421"
date: 2024-01-31
language:
  - java
  - cpp
title: Big O notation
updated: 2024-03-25T13:46
---
# [[Big O notation]]
- compares diff algorithms
	- how ugly they get as `n` gets bigger (`n` = amount of data)
- machine independent
- ignores smaller operations

> [!example]
> simple for loop: would be $O(n)$, where $n = number\ of\ characters\ in\ string$ 


> [!example] From slowest -> fastest:
> *reference graph here: [[big-o-notation-graph-examples.png]]*
> - $O(1)$ = constant time
> - $O(log n)$ = logarithmic time
> - $O(n)$ = linear time
> - $O(n log n)$ = quasilinear time
> - $O(n^2)$ = quadratic time
> - $O(n!)$ = factorial time
> 
> Something to note is that some "slower" algorithms can be faster when working with **smaller datasets**.
> 

![[big-o-complexity-chart.png]]
%%thanks Frostbiiten (Edem) lmao%%


___
# References
- https://usaco.guide/bronze/time-comp?lang=java
- https://www.youtube.com/watch?v=XMUe3zFhM5c
- [[typical-big-o-notation-speeds-for-diff-n-values.png]]