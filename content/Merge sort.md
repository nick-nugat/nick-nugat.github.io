---
aliases: "202403251338"
tags: 
date: 2024-03-25
created: 2024-03-25T13:38
updated: 2024-03-25T13:54
---
# [[Merge sort]]
- Continuously cuts array in half until it can't anymore.
- With one element, an array is always sorted.
- On both sides of the array, sort the subarrrays.
- When finished, merge everything back together in the correct order.

![[merge-sort-example-image.png|500]]

```java
private static void mergeSort(int[] arr) {
	int length = arr.length;
	int midIndex = arr.length / 2;

	if (length < 2) return; //during recursive calls, when the input array length is less than 2, the method finishes

	int[] leftHalf = new int[midIndex];
	int[] rightHalf = new int[length - midIndex];

		//copy elements from arr to leftHalf
	for (int i = 0; i < midIndex; i++) {
		leftHalf[i] = arr[i];
	}

	//copy second half of elements from arr to rightHalf
	for (int i = midIndex; i < length; i++) {
		rightHalf[i - midIndex] = arr[i];
	}

	//recursive calls to mergeSort()
	mergeSort(leftHalf);
	mergeSort(rightHalf);

	//merge array halves together
	merge(arr, leftHalf, rightHalf);
}

public static void merge(int[] arr, int[] leftHalf, int[] rightHalf){
	int leftLength = leftHalf.length;
	int rightLength = rightHalf.length;

	/*
	iterators:
	i - left
	j - right
	k - merged
	*/
	int i = 0, j = 0, k = 0;

	while (i < leftLength && j < rightLength){
		if (leftHalf[i] <= rightHalf[j]){
			arr[k] = leftHalf[i];
			i++;
		} else {
			arr[k] = rightHalf[j];
			j++;
		}
		k++;
	}

	while(i < leftLength){
		arr[k] = leftHalf[i];
		i++;
		k++;
	}

	while(j < rightLength){
		arr[k] = rightHalf[j];
		j++;
		k++;
	}
}
```

___
# References
https://www.geeksforgeeks.org/merge-sort/
