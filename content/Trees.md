---
aliases:
  - "202403052301"
language:
  - java
date: 2024-03-05
created: 2024-03-05T23:01
updated: 2024-03-06T01:17
---
# [[Trees]]
Trees are a form of hierarchical way of organization.

```java
/** An example interface of basic methods for the ADT tree.  */
public interface TreeInterface<T>{
   public T getRootData();
   public int getHeight();
   public int getNumberOfNodes();
   public boolean isEmpty();
   public void clear();
} // end TreeInterface
```

## Visual examples
> [!example]-
> ![[family-tree.png|350]]
> ![[folder-tree.png|350]]
> ![[terminology-in-trees.png|350]]
> ![[binary-tree-example.png|350]]
> ![[three-binary-trees-in-different-states-of-completion.png|350]]

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
![[binary-tree-traversal-types.png|350]]

> [!example]- Example of preorder and postorder in a general tree
> ![[binary-tree-preorder-and-postorder-traversal-examples.png|350]]
#### In-order
> [!warning] This is not ideal for general tree traversal!

![[binary-tree-in-order-traversal.png|350]]

#### Preorder
![[binary-tree-preorder-traversal.png|350]]

#### Postorder
![[binary-tree-postorder-traversal.png|350]]

#### Level-order
![[binary-tree-level-order-traversal.png|350]]

## Binary trees
Binary trees are trees where **each node** has at most *two children*.
### Example
```java
BinaryTreeInterface<String> dTree = new BinaryTree<>();
dTree.setTree("D", null, null);

BinaryTreeInterface<String> fTree = new BinaryTree<>();
fTree.setTree("F", null, null);

BinaryTreeInterface<String> gTree = new BinaryTree<>();
gTree.setTree("G", null, null);

BinaryTreeInterface<String> hTree = new BinaryTree<>();
hTree.setTree("H", null, null);

BinaryTreeInterface<String> emptyTree = new BinaryTree<>();

// Form larger subtrees
BinaryTreeInterface<String> eTree = new BinaryTree<>();
eTree.setTree("E", fTree, gTree); // Subtree rooted at E

BinaryTreeInterface<String> bTree = new BinaryTree<>();
bTree.setTree("B", dTree, eTree); // Subtree rooted at B

BinaryTreeInterface<String> cTree = new BinaryTree<>();
cTree.setTree("C", emptyTree, hTree); // Subtree rooted at C

BinaryTreeInterface<String> aTree = new BinaryTree<>();
aTree.setTree("A", bTree, cTree); // Desired tree rooted at A

// Display root, height, number of nodes
System.out.println("Root of tree contains " + aTree.getRootData());
System.out.println("Height of tree is " + aTree.getHeight());
System.out.println("Tree has " + aTree.getNumberOfNodes() + " nodes");

// Display nodes in preorder
System.out.println("A preorder traversal visits nodes in this order:");
Iterator<String> preorder = aTree.getPreorderIterator();
while (preorder.hasNext())
   System.out.print(preorder.next() + " ");
System.out.println();
```

![[visualization-of-binary-tree-build-example.png]]


### Types
#### Expression trees
Trees can also represent algebraic expressions.

![[expression-trees.png|350]]
![[expression-tree-evaluation-algorithm.png|350]]

#### Decision trees
These can be used for things like a guessing game.
![[decision-trees-for-a-guessing-game.png|350]]

#### Search tree
- each node in a binary search tree:
	- node's data is **greater than** all data in node's left subtree
	- node's data is **less than** all data in node's right subtree
- every node is **the root** of a binary search tree
##### Efficiency of search
- Searching a binary search tree is $O(h)$, where $h$ is height.
	- The operations add, remove, and getEntry are O(h)
- If tree of $n$ nodes has height $h = n$, these operations are $O(n)$
- Increase efficiency by making sure tree is as short as possible.

- Shortest tree is full
	- Results in these operations being $O(\log n)$

![[two-binary-search-trees-with-different-searching-effeciencies.png|350]]


___

### Traversing
#### Using a Stack ([[#Preorder]] and [[#Postorder]])
![[traversing-binary-tree-using-stack.png|350]]

#### Using a Queue ([[#Level-order]])
![[traversing-binary-tree-with-queue.png|350]]

# References
