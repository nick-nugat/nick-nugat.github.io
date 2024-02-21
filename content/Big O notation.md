---
aliases:
  - "202401311421"
date: 2024-01-31
language:
  - java
  - cpp
title: Big O notation
updated: 2024-02-21T14:25
---
# [[Big O notation]]
## Notes
> [!NOTE]- sorting algorithm speeds:
> - bubble sort $\dfrac{(n^2 - n)}{2}$
> - insertion sort: $\dfrac{n^2}{2}$
> - selection sort: $\dfrac{(n^2 - -n)}{2}$
> - merge sort: $nlogn$

> [!example]
> simple for loop: would be $O(n)$, where $n = number\ of\ characters\ in\ string$ 

- compares diff algorithms
	- how ugly they get as `n` gets bigger (`n` = amount of data)
- machine independent
- ignores smaller operations

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





## References
- https://usaco.guide/bronze/time-comp?lang=java
- https://www.youtube.com/watch?v=XMUe3zFhM5c
- [[typical-big-o-notation-speeds-for-diff-n-values.png]]