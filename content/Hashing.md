---
updated: 2024-02-26T14:27
aliases:
  - Hash tables
---
# Hashing
## Hash tables
- hash tables can be used to locate elements in a [[Data structures|data structure]] without searching linearly
## Hash functions
- hash functions compute an integer value (hash code) from an object in the hash table
	- common way to scale integer is to use the `%` (modulo) operator
- search key is mapped, or hashed, to the index


```java
code % n //good to use an odd num for `n`
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

#### Three kinds of locations on hash table
1. occupied
2. empty (null or never contained anything)
3. available
