---
aliases:
  - "202403052301"
language: 
date: 2024-03-05
created: 2024-03-05T23:01
updated: 2024-03-06T00:14
---
# [[Trees]]
Trees are a form of hierarchical way of organization.

## Visual examples
> [!example]-
> ![[family-tree.png]]
> ![[folder-tree.png]]
> ![[terminology-in-trees.png]]
> ![[binary-tree-example.png]]
> ![[three-binary-trees-in-different-states-of-completion.png]]

## Tree terminology
- "roots" are at the top and they are the only node with **no parent**.
- trees can be empty
- height = num of levels

## Traversing a tree
- each item is visited **exactly once**
- order of traversal is **NOT unique**
- uses **recursion**
- to visit all nodes
	- visit root
	- visit all nodes on **root's *left* subtree**
	- visit all nodes on **root's *right* subtree**

### Types of traversals
![[binary-tree-traversal-types.png]]

> [!example]-
> ![[binary-tree-preorder-traversal.png]]
> ![[binary-tree-in-order-traversal.png]]
> ![[binary-tree-postorder-traversal.png]]
> ![[Pasted image 20240306001442.png]]

___
## References
