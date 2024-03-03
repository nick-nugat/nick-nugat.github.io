---
updated: 2024-03-03T16:52
aliases:
  - Hash tables
  - Hash functions
---
# [[Hashing]]
## Hash tables
- hash tables can be used to locate elements in a [[Data structures|data structure]] without searching linearly
## Hash functions
- hash functions compute an integer value (hash code) from an object in the hash table
	- common way to scale integer is to use the `%` (modulo) operator
- search key is mapped, or hashed, to the index

```java
code % n //good to use an odd num for `n`
```

```java
/*compressing a hash code*/
private int getHashIndex(K key){
   int hashIndex = key.hashCode() % hashTable.length;
   if (hashIndex < 0)
      hashIndex = hashIndex + hashTable.length;
      
   return hashIndex;
} // end getHashIndex
```
## Examples
### Computing hash code from object `x`
```java
int h = x.hashCode();
```

###  Identifying students
- use their student id because it's unique

## [[Hashing collisions]]

# References
- [Introduction to Hashing - Data Structure and Algorithm Tutorials - GeeksforGeeks](https://www.geeksforgeeks.org/introduction-to-hashing-data-structure-and-algorithm-tutorials/)
	- [*highlights here*](obsidian://open?vault=NguyenN_Vault&file=_inbox%2Fomnivore%2FIntroduction%20to%20Hashing%20-%20Data%20Structure%20and%20Algorithm%20Tutorials%20-%20GeeksforGeeks)