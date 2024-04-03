---
aliases:
  - "202404011340"
language:
  - java
date: 2024-04-01
created: 2024-04-01T13:40
updated: 2024-04-03T13:48
---
# [[Graph]]

> [!tldr] Definition
> A collection of distinct vertices and distinct edges. 

They are an extension of [[Tree]]s in the sense that every [[Tree]] is a graph but not every graph is a tree.


![[slide-abt-what-a-graph-is.png]]

___
## Paths
- path b/t two vertices in a graph is a sequence of edges
- **directed path** - paths in a directed graph must consider the direction of edges
- **length** of a path is num of edges it comprises
- **cycle** of a path - begins and ends at same point

![[examples-of-undiredcted-graphs-to-demonstrate-paths.png]]

## Types of graphs
### Connected graphs
**Has a path between every pair** of distinct vertices - can visit any other node.
### Disconnected graphs
At least one node can't be reached.
### Complete graph
Each node has an **edge (line) to every other node**.

### Undirected graphs
Where edges have **no direction** (no arrows) - nodes are unordered pairs in the definition of every edge.
- can be [[#Connected graphs|connected]], [[#Complete graph|complete]], or disconnected

![[example-of-directed-graph-and-weighted-graph.png]]

### Directed graphs
Where edges have **direction** (has arrows) - nodes are ordered pairs in the definition of every edge.
![[example-of-directed-graphs_airline-routes.png]]

## Graph traversals
![[examples-of-preorder-and-level-order-graph-traversals.png]]



___
# References
- [Graph Data Structure And Algorithms - GeeksforGeeks](https://www.geeksforgeeks.org/graph-data-structure-and-algorithms/)
- [Eulerian path and circuit for undirected graph - GeeksforGeeks](https://www.geeksforgeeks.org/eulerian-path-and-circuit/)