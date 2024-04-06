---
aliases:
  - "202404031744"
language:
  - java
date: 2024-04-03
created: 2024-04-03T17:44
updated: 2024-04-06T14:42
---
# [[Midterm 2 review]]
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
1) **Ranking Big-O Notations:**
   a. O(log n)
   f. O(1)
   d. O(n)
   a. O(n log n)
   b. O(n^2)
   g. O(2^n)
   e. O(n!)
   
   Explanation:
   - O(1) represents constant time complexity, which is the fastest.
   - O(log n) is generally faster than linear time complexity O(n).
   - O(n log n) is often encountered in efficient sorting algorithms like merge sort and quicksort.
   - O(n^2) denotes quadratic time complexity, which is slower than linear and n log n time complexities.
   - O(2^n) represents exponential time complexity, considerably slower.
   - O(n!) represents factorial time complexity, which is the slowest.

2) **Computational Complexity:**
   The computational complexity of the given function \( n^3 + 30n \log n + 12000 \) is \( O(n^3) \). In Big-O notation, we typically focus on the dominant term, which is \( n^3 \) in this case.

3) **Critical Section in Calculating Computational Complexity:**
   The critical section in calculating computational complexity is typically the part of the algorithm or function that dominates the runtime as the input size grows. This section determines the overall complexity of the algorithm.

4) **Converting Binary Tree to Array:**
   To convert a binary tree to an array using the 2i+1/2i+2 rule, you can traverse the tree in level order (BFS) and store the nodes in the array according to the formula. This ensures that for any node at index i in the array, its left child will be at index 2i+1 and its right child will be at index 2i+2.

5) **Heap Operations:**
   To convert an existing heap after inserting or deleting a node, you typically perform heapify operations. For insertion, you perform an "up-heap" operation (also known as "heapify up") to maintain the heap property. For deletion, you perform a "down-heap" operation (also known as "heapify down") to rearrange the elements and maintain the heap property.

6) **Sets and Maps Operations in Java:**
   ```java
   // Adding a mapping to a key-value mapping (Map)
   Map<KeyType, ValueType> map = new HashMap<>();
   map.put(key, value);

   // Displaying each value and key
   for (Map.Entry<KeyType, ValueType> entry : map.entrySet()) {
       System.out.println("Key: " + entry.getKey() + ", Value: " + entry.getValue());
   }
   ```

7) **Valid Hash Codes for a Class:**
   A valid hash code for a class should return an integer value. It should follow the contract specified by the `hashCode()` method in Java, which states that equal objects must produce the same hash code, but unequal objects may or may not produce the same hash code.

8) **Hash Code Contract:**
   A class satisfies the hash code contract if it correctly implements the `hashCode()` method according to the contract defined in the Java documentation. This includes ensuring that equal objects have the same hash code and implementing a consistent hash code calculation.

9) **Fastest Sorting Algorithms (in Big-O):**
   - The fastest sorting algorithm in Big-O notation is O(n log n), which includes algorithms like merge sort, heap sort, and quicksort in their average and best cases.

10) **Fastest Search Algorithms (in Big-O):**
    - The fastest search algorithm in Big-O notation depends on the data structure used. For sorted arrays/lists, binary search (O(log n)) is the fastest. For unsorted collections, linear search (O(n)) is typically the best we can achieve.

11) **Making a Class Generic:**
    To make a class generic in Java, you can use type parameters. For example:
    ```java
    public class MyClass<T> {
        private T data;

        public MyClass(T data) {
            this.data = data;
        }

        public T getData() {
            return data;
        }

        public void setData(T data) {
            this.data = data;
        }
    }
    ```

12) **Inserting/Retrieving a Node from a Binary Search Tree:**
    - To insert a node into a binary search tree (BST), you traverse the tree recursively, comparing the value of the node to be inserted with the values of existing nodes until you find the appropriate position to insert.
    - To retrieve a node from a BST, you perform a similar recursive traversal, comparing the value you're searching for with the values of nodes in the tree until you find the desired node or determine that it does not exist in the tree.

13) **Writing a Recursive Method:**
    Here's a simple example of a recursive method to calculate the factorial of a number:
    ```java
    public static int factorial(int n) {
        if (n == 0 || n == 1) {
            return 1;
        } else {
            return n * factorial(n - 1);
        }
    }
    ```

14) **Iterators:**
    Iterators in Java provide a way to access elements of a collection sequentially without exposing the underlying data structure. They typically have methods like `hasNext()` to check if there are more elements and `next()` to retrieve the next element. Iterators are commonly used in loops to traverse collections such as lists, sets, and maps.



___


# References
