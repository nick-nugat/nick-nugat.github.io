---
aliases: "202403251322"
tags: 
date: 2024-03-25
created: 2024-03-25T13:22
updated: 2024-03-25T14:03
---
# [[Bubble sort]]
- Value pairs are sorted continuously; array continues to loop **in its entirety** until all pairs are sorted.
- Values "bubble" to the top.

```java
private static void bubbleSort(int[] arr){
	int length = arr.length;
	boolean sorted = true;

	//checks if list needs to be sorted again
	while (sorted){
		sorted = false;
		for (int i = 0; i < length - 1; i++) {
			int currentValue = arr[i];
			int nextValue = arr[i + 1];

			if (currentValue > nextValue){
				swap(arr, i, i + 1); //swaps values at index i and index i + 1
				sorted = true;
			}
		}
	}
}
```

___
# References
https://www.programiz.com/dsa/bubble-sort