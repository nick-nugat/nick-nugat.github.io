---
aliases: "202403181407"
language: 
date: 2024-03-18
created: 2024-03-18T14:07
updated: 2024-03-20T14:18
---
# [[Sets]]
- unordered list of items
- no duplicates
	- adding an element **does nothing** if it already exists in the set
	- removing an element that's not in the set is **ignored**

## Operations
- union
- intersection
- difference

![[three-basic-set-operations.png|300]]
![[union-intersection-difference_example-with-two-sets.png|500]]
## Implementing
### Explicit (bit vector)
- each item in base type has representation in each instance of a set
	- representation either true or false (item in set or not)
- space is proportional to the cardinality of the base type
	- all bit vectors use same amount of memory regardless of how many elements there are
- algorithms use boolean operations

![[explicit-set-example.png|500]]
### Implicit






___
# References
