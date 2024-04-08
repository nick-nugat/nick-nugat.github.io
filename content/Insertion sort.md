---
aliases:
  - "202403251324"
language: []
date: 2024-03-25
created: 2024-03-25T13:24
updated: 2024-04-07T20:39
---
# [[Insertion sort]]
- Consider the first element sorted; start at the second element
- Compare to previous elements

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