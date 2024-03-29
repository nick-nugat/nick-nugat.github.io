---
aliases: "202403281120"
type: design
language: java
date: 2024-03-28
created: 2024-03-28T11:20
updated: 2024-03-29T17:47
---
# [[assignment5-design-initial]]

> Nicholas Nguyen

___
%%
## GitHub screenshot

## Learning experience
%%

## UML diagram
```mermaid
classDiagram
direction BT

class TreeNode~T~{
	- leftChild: T
	- rightChild: T
	- data: T
	
	+ TreeNode(T dataNode)
	+ TreeNode(TreeNode<T> node)
	+ getData() T
}


class LinkedConverterTreeInterface~String~{
	<<interface>> 
}

class MorseCodeTree{
	+ MorseCodeTree()
	+ getRoot() TreeNode~String~
	+ setRoot(newNode: TreeNode~String~) void
	+ insert(code: String, letter: String) void
	+ addNode(root: TreeNode~String~, code: String, letter: String) void
	+ fetch(code: String) String
	+ fetchNode(root: TreeNode~String~, code: String)
	+ buildTree() void
	+ toArrayList() ArrayList~String~

	%%throws UnsupportedOperationException
	+ delete(data: String) MorseCodeTree
	+ update() MorseCodeTree
}

LinkedConverterTreeInterface~String~ <|-- MorseCodeTree: implements

class MorseCodeConverter{
	+ MorseCodeConverter()
	+ printTree() String
	+ convertToEnglish(code: String) String

	%%throws FileNotFoundException
	+ convertToEnglish(codeFile: File) String
}

```

## Pseudocode
This program is one that serves to convert Morse Code into English.


