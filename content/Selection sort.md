---
aliases:
  - "202404031747"
language: []
date: 2024-04-03
created: 2024-04-03T17:47
updated: 2024-04-07T20:26
---
# [[Selection sort]]
- Traverses whole array to find minimum -> swap.
- Continuously traverse through the rest of the **unsorted** array section, continuing to find the minimum of that part of the array.
- Continue until array is fully sorted.


```java
//loops array multiple times, finding the smallest value from where its index is and swapping it
private static void selectionSort(int[] arr) {
	int length = arr.length;

	for (int i = 0; i < length; i++) {
		int minValue = arr[i];
		int indexOfMin = i;
		for (int j = i + 1; j < length; j++){
			if (arr[j] < minValue){
				minValue = arr[j];
				indexOfMin = j;
			}
		}
		swap(arr, i, indexOfMin);
	}
}
```





___
# References
[Selection Sort – Data Structure and Algorithm Tutorials - GeeksforGeeks](https://www.geeksforgeeks.org/selection-sort/)