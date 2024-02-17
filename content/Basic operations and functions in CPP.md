---
aliases: 
date: 2024-02-17
language: 
updated: 2024-02-17T06:22
title: Basic operations and functions in CPP
---
## `cin` - practically equivalent of Java Scanner
- prompts user to enter value

```cpp
// C++ program to demonstrate the
// cin object
#include <iostream>
using namespace std;

// Driver Code
int main()
{
	string s;

	// Take input using cin
	cin >> s;

	// Print output
	cout << s;

	return 0;
}

```

## Type casting
**Format**:

```cpp
static_cast<DataType>(Value)
```


## setw() stream manipulator
- `#include <iomanip>`
- used to set width of the space to print (cout)

## setprecision() function
- `#include <iomanip>`
- used to set amount of sig figs in a float/double
- use `fixed` keyword to only target numbers after decimal point
