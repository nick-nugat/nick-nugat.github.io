---
aliases:
  - "202404031744"
  - CMSC204 exam 2
  - CMSC204 Midterm II
language:
  - java
date: 2024-04-03
created: 2024-04-03T17:44
updated: 2024-04-06T15:12
---
# [[CMSC204 Midterm 2 Review]]
## Topics/questions

1)	Rank a set of Big-O notations
a.	O(n log n)
b.	O(n2)
c.	O(log n)
d.	O(n) 
e.	O(n!) 
f.	O(1) 
g.	O(2n) 
2)	What is the computational complexity of the following function? n3+30nlogn + 12000
3)	Identify the “critical section” in calculating computational (asymptotic) complexity.
4)	Convert a binary tree to an array using the 2i+1/2i+2 rule.
5)	Convert an existing heap into a heap that results from inserting or deleting a node.
6)	Sets and Maps: Write code that adds a mapping to a key-value mapping; write code that displays each value and key
7)	Identify valid hash-codes for a class (returns an int)
8)	Does a given class satisfy the hash-code contract?
9)	Identify the fastest (in Big-O) of a set of sort algorithms
10)	Identify the fastest (in Big-O) of a set of search algorithms
11)	Modify a class to make it generic
12)	Insert/retrieve a node from a binary search tree
13)	Write a recursive method.
14)	Iterators


## Answers from Bing Copilot
Certainly! Let’s tackle each of these questions step by step:

1. **Ranking Big-O Notations**:
    
    - Here’s the ranking from fastest to slowest:
        - **f. O(1)** (constant time complexity)
        - **c. O(log n)** (logarithmic time complexity)
        - **d. O(n)** (linear time complexity)
        - **a. O(n log n)** (linearithmic time complexity)
        - **b. O(n^2)** (quadratic time complexity)
        - **g. O(2^n)** (exponential time complexity)
        - **e. O(n!)** (factorial time complexity)
2. **Computational Complexity of the Given Function**:
    
    - The given function is:
        
        f(n) = n^3 + 30n \log n + 12000f(n)=n3+30nlogn+12000
        
    - In Big-O notation, we typically focus on the dominant term. Here, the dominant term is
        
        n^3n3
        
        .
    - [Therefore, the computational complexity of this function is **O(n^3)**](https://www.chegg.com/homework-help/questions-and-answers/computational-complexity-following-function-n3-30nlogn-12000-q41674721) [1](https://www.chegg.com/homework-help/questions-and-answers/computational-complexity-following-function-n3-30nlogn-12000-q41674721)[2](https://nick-nugat.github.io/coding-notes/Midterm-2-review).
3. **Critical Section in Calculating Computational Complexity**:
    
    - The critical section in calculating computational (asymptotic) complexity is the part of the algorithm or function that contributes the most to the overall time complexity.
    - It’s the portion of code that dominates the runtime as the input size grows.
4. **Converting a Binary Tree to an Array**:
    
    - To convert a binary tree to an array, you can use the 2i+1/2i+2 rule.
    - Start at the root (index 0) and follow these steps:
        - The left child of node i is at index 2i+1.
        - The right child of node i is at index 2i+2.
    - Repeat this process for each level of the tree until you’ve covered all nodes.
5. **Converting an Existing Heap**:
    
    - When inserting or deleting a node in a heap, you need to maintain the heap property (either min-heap or max-heap).
    - For insertion, add the new node at the end and then “bubble up” (swap with parent) until the heap property is satisfied.
    - For deletion, replace the root with the last node, and then “bubble down” (swap with the smaller child) until the heap property is restored.
6. **Sets and Maps**:
    
    - To add a mapping to a key-value mapping:
        - In a map (dictionary), assign a value to a key.
        - In a set, simply add an element.
    - To display each value and key:
        - Iterate through the map or set and print the key-value pairs.
7. **Valid Hash-Codes for a Class**:
    
    - A valid hash code for a class (which returns an integer) should be consistent (same value for the same object) and follow the contract:
        - If two objects are equal (according to their `equals` method), their hash codes must be the same.
        - However, the reverse is not necessarily true (two unequal objects can have the same hash code).
8. **Hash-Code Contract**:
    
    - A class satisfies the hash-code contract if it adheres to the rules mentioned above.
9. **Fastest Sort Algorithms (in Big-O)**:
    
    - The fastest sorting algorithms are:
        - **QuickSort**: Average case: O(n log n).
        - **MergeSort**: Always: O(n log n).
10. **Fastest Search Algorithms (in Big-O)**:
    
    - The fastest search algorithm is:
        - **Binary Search**: O(log n).
11. **Making a Class Generic**:
    
    - To make a class generic, use type parameters (e.g., `class MyClass<T>`).
    - Replace specific types with the type parameter throughout the class.
12. **Inserting/Retrieving Nodes from a Binary Search Tree**:
    
    - To insert a node, compare the value with the root and recursively insert it in the left or right subtree.
    - To retrieve a node, follow the same comparison process until you find the desired node.
13. **Writing a Recursive Method**:
    
    - A recursive method calls itself during its execution.
    - Example: Writing a recursive factorial function:
        
        \text{factorial}(n) = n \cdot \text{factorial}(n-1)factorial(n)=n⋅factorial(n−1)
        
        .
14. **Iterators**:
    
    - Iterators allow you to traverse a collection (e.g., list, set, map) sequentially.
    - They provide methods like `next()` to retrieve the next element.

Feel free to ask if you need further clarification on any of these topics! Good luck with your midterm! 📚👍



___


# References
