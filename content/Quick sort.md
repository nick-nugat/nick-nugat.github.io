---
aliases: "202403251401"
tags: 
date: 2024-03-25
created: 2024-03-25T14:01
updated: 2024-03-25T14:01
---
# [[Quick sort]]

```java
//overloaded method for simpler method call
private static void quickSort(int[] arr){
	quickSort(arr, 0, arr.length - 1);
}
//recursive type of method - random index is the "pivot" - takes values less than and greater than pivot and places them on left and right of it respectively - continues doing same thing for its sub-arrays
private static void quickSort(int[] arr, int lowIndex, int highIndex){
	if (lowIndex >= highIndex) return;

	//choosing pivot randomly
	int pivotIndex = new Random().nextInt(highIndex - lowIndex) + lowIndex;

	//setting pivot to random index in array
	int pivot = arr[pivotIndex];

	//swapping value at pivotIndex with value at highIndex
	swap(arr, pivotIndex, highIndex);

	int leftPointer = partition(arr, lowIndex, highIndex, pivot); //partitions array

	//recursive - sorts left sub-array
	quickSort(arr, lowIndex, leftPointer - 1);

	//recursive - sorts right sub-array
	quickSort(arr, leftPointer + 1, highIndex);
}

private static int partition(int[] arr, int lowIndex, int highIndex, int pivot) {
	int leftPointer = lowIndex;
	int rightPointer = highIndex;

	//move left and right pointers towards each other until they hit each other :p
	while (leftPointer < rightPointer){
		//while value at leftPointer in array is <= the pivot AND the leftPointer is less than the rightPointer, INCREMENT the leftPointer
		while ((arr[leftPointer] <= pivot) && (leftPointer < rightPointer))
			leftPointer++;
		//while value at rightPointer in array is >= the pivot AND the leftPointer is less than the rightPointer, DECREMENT the rightPointer
		while ((arr[rightPointer] >= pivot) && (leftPointer < rightPointer))
			rightPointer--;

		swap(arr, leftPointer, rightPointer);
	}
	swap(arr, leftPointer, highIndex);

	return leftPointer;
}
/**
 * Swaps two values in an array
 * @param arr Array whose values need to be swapped
 * @param a Index to swap
 * @param b Index to swap
 */
private static void swap(int[] arr, int a, int b){
	int temp = arr[a];
	arr[a] = arr[b];
	arr[b] = temp;
}
```