---
updated: 2024-02-28T14:12
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

## Collisions
- happens when a hash function maps a search key into a location the hash table is already using
### Resolving them
1. use another location in hash table
2. change hash table structure so array can represent more than one value

#### Linear probing
hash table is searched **sequentially**.
- if location is **occupied**, search the *next* location

> [!NOTE] Algorithm
> 1. Calculate the hash key. i.e. **key = data % size**
> 2. Check, if **hashTable[key]** is empty
>     - store the value directly by **hashTable[key] = data**
> 3. If the hash index already has some value then
>     1.  check for next index using **key = (key+1) % size**
> 4. Check, if the next index is available hashTable[key] then store the value. Otherwise try for next index.
> 5. Do the above process till we find the space.


> [!example]-
> ![[linear-probing-example.png]]


#### Quadratic probing
Searches thorugh 

##### Example sequence
$$H + 12, H + 22, H + 32, H + 42…………………. H + k2$$




> [!example]-
> ![[quadratic-probing-example.png]]

#### Buckets
#### Clustering

### Three kinds of locations on hash table
1. occupied
2. empty (null or never contained anything)
3. available

# References
- [Introduction to Hashing - Data Structure and Algorithm Tutorials - GeeksforGeeks](https://www.geeksforgeeks.org/introduction-to-hashing-data-structure-and-algorithm-tutorials/)