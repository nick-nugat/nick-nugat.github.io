---
aliases: 
date: 2024-02-17
language: 
updated: 2024-02-21T11:37
title: Data types in CPP
---
# Data types
### Integers
- you can use **digit separators** to improve readability. use `'` (single quotes)
	- `int count = 1'000'000;`


### Strings
> [!important]
> - use `#include <string>` if you want to use strings (though `<iostream>` already includes this so no need to declare separately)
> - unlike Java, `string` is lowercase

### Floating point data types
- three types
	- `float` %%single precision%%
	- `double` %%double precision - typically twice as big as float%%
	- `long double` %%larger than double%%

### Bool value
> [!important]
> - Unlike in Java, booleans are declared as `bool` in C++
> - `true` is represented by 1, `false` is represented by 0

### Finding size of data type
- use `sizeof` operator to find if you forget
	- syntax: `sizeof(int)` - in parentheses, insert data type of name of variable

### Auto data type
- keyword `auto` tells the compiler to determine the variable's data type based on the initialization value

### Named constants
- preface code with `const` before declaring data type/initializing
- contents are **read-only**
- *similar to Java's `final` keyword*
