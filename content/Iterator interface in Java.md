---
aliases:
  - "202402211323"
date: 2024-02-21
language:
  - java
created: 2024-02-21T13:23
updated: 2024-02-21T13:59
---
# [[Iterator interface in Java]]

## Methods
- `hasNext()`: boolean
	- returns true if next element exists
- `next()`:  T
	- returns next element
- `remove()`: void
	- deletes element *before* cursor 
	- cursor doesn't move

## Implementation
### Inside data structure class (inner class)
- internal iterator
- data structure’s encapsulation
### Outside data structure class
- external iterator
- `Iterator` class can be used in multiple data structures
- implementation unencapsulates the data structure




## Multiple iterators
> [!example]
> ![[working-with-multiple-iterators.png|500]]
> In this example, nested while-loops are used to count both a certain name and the amount of times it appears in a certain iterator.





___
## References
- [[Module 11 - Iterators and Interfaces.pptx]]