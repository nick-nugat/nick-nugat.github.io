---
aliases: "202404031846"
tags: 
date: 2024-04-03
created: 2024-04-03T18:46
updated: 2024-04-03T18:49
---
# [[Binary tree sort]]
Sorted items are inserted into a [[Tree#Binary trees#Search tree|Binary search tree]]
- An LNR (inorder) traversal visits the items in ascending order
- An RNL traversal visits the items in decending order

Notes:
- Does not swap anything
- Lots of overhead

Process:
1. The first item becomes the root node.
2. For any subsequent item, consider the root node to be a root of a subtree, and start at the root of this subtree.
3. Compare the item to the root of the subtree.
	1. If the new item is less than the subtree’s root, then	  the new subtree is the root’s left subtree
	2. Else the new subtree is the root’s right subtree.
4. Repeat step 3 until the new subtree is empty. Position the new item as the root of this empty subtree.
5. Repeat steps 2, 3 and 4 for each item to be sorted

An LNR (inorder) traversal Outputs the items in ascending order
