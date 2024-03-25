---
aliases: 
date: 2024-01-29
language: java
updated: 2024-03-25T10:53
title: Generics in Java
---
# [[Generics in Java]]
- type parameter (typically `<T>` by convention)
- can be classes or methods
	- **methods** can be defined inside *non-generic classes*

example:
- interface `Comparable`
	- if `s` and `t` are strings, has method `s.compareTo(t)`
		- Negative if s comes before t
		- Zero if s and t are equal
		- Positive if s comes after t

- can declare multiple generic types separated by comma (`,`)
## Bounded type parameters
### Examples:

> [!Fail]- Incorrect
```java
public MyClass
{
   // First draft and INCORRECT:
   public static <T> T arrayMinimum(T[] anArray)
   {
      T minimum = anArray[0];
      for (T arrayEntry : anArray)
      {
         if (arrayEntry.compareTo(minimum) < 0)
            minimum = arrayEntry;
      } // end for
      return minimum;
   } // end arrayMinimum
} // end MyClass
```

> [!check]- Correct
```java
public MyClass
{
   public static <T extends Comparable<T>> T arrayMinimum(T[] anArray)
   {
      T minimum = anArray[0];
      for (T arrayEntry : anArray)
      {
         if (arrayEntry.compareTo(minimum) < 0)
            minimum = arrayEntry;
      } // end for
      return minimum;
   } // end arrayMinimum
   // . . .
} // end MyClass
```

___
## Wildcards
- represents an **unknown class type** with a `?`

## Type erasure
![[Pasted image 20240131143949.png]]
![[Pasted image 20240131144002.png]]
- cannot make arrays of generic type -> *use arraylist instead if needed*
	- only works in parameter because the array has already been constructed