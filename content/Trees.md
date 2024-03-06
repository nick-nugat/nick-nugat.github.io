---
aliases:
  - "202403052301"
language:
  - java
date: 2024-03-05
created: 2024-03-05T23:01
updated: 2024-03-06T00:44
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

> [!example]- Example of preorder and postorder in a general tree
> ![[binary-tree-preorder-and-postorder-traversal-examples.png]]
#### In-order
> [!warning] This is not ideal for general tree traversal!

![[binary-tree-in-order-traversal.png]]

#### Preorder
![[binary-tree-preorder-traversal.png]]

#### Postorder
![[binary-tree-postorder-traversal.png]]

#### Level-order
![[binary-tree-level-order-traversal.png]]

## Tree interface
```java
/** An interface of basic methods for the ADT tree.  */
public interface TreeInterface<T>{
   public T getRootData();
   public int getHeight();
   public int getNumberOfNodes();
   public boolean isEmpty();
   public void clear();
} // end TreeInterface
```

## Binary trees
Binary trees are trees where **each node** has at most *two children*.

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






### Expression trees
Trees can also represent algebraic expressions.

![[expression-trees.png]]
![[expression-tree-evaluation-algorithm.png]]




## References
