---
aliases: 
date: 2024-01-31
language: java
updated: 2024-02-17T06:22
title: Data structures
---
# [[Data structures]]
- Data structures are an implementation of an ADT (abstract data type).
## ADT bags
- finite collection of items in no order
- can have duplicates
## What is abstraction?
- "The idea of knowing how to use something without knowing how it is implemented"
- **Types:**
	- procedural abstraction
	- data abstraction

___
## Nodes
- contains data; one or more links to other nodes
- can be used to represent structures like **linked lists** and **trees**
- **Types:**
	- orphaned nodes - no links pointing to them except for head node
	- null node - " A `NULL` value in the link part of a node’s info denotes that the path or data structure contains no further nodes."

___

> [!NOTE] 4 operations:
> - insert
> - delete
> - modify/update
> - query

## Stack
> LIFO (last in, first out)

> [!example]
> The last item inserted is the first item out (like a stack irl).

- pop() -> removes top element
	- delete
	- query
- push() -> adds element to top
	- insert
- peek() -> returns element on top
### When would I want to use a Stack?
- making sure parentheses line up in an expression
	- if nothing on stack -> everything lines up
	- otherwise, there was a left parenthesis not aligned correctly

## Queue
> FIFO (first in, first out)

> [!example]
> In a line, the first person in (waiting the longest) is the first person out.



___
## References
- https://www.codecademy.com/learn/getting-started-with-data-structures-java/modules/nodes-java/cheatsheet
- [[Module 01 - Data Structure ADT(1).pptx]]