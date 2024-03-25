---
aliases: "202403251324"
tags: 
date: 2024-03-25
created: 2024-03-25T13:24
updated: 2024-03-25T13:43
---
# [[Insertion sort]]
- Checks pair of values -> **is value greater than previous value greater?** -> swap values.
- Restarts iteration.
- Iterates again.
- This continues until all values are sorted.

```java
private static void insertionSort(int[] arr){
	int length = arr.length;

	for (int i = 1; i < length; i++) {
		int currentValue = arr[i]; //saving current value off to a temporary variable

		int j = i - 1;
		while (j >= 0 && arr[j] > currentValue){
			arr[j + 1] = arr[j];
			j--;
		}
		arr[j + 1] = currentValue;
	}
}
```


___
# References
https://www.geeksforgeeks.org/insertion-sort/