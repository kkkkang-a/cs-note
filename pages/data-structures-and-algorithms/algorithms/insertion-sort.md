# Insertion Sort

Insertion sort is a sorting algorithm that builds the final sorted array (or list) one element at a time.

It works by repeatedly taking the next element from the unsorted part of the array and inserting it into its correct position within the sorted part of the array.

## Algorithm

1. **Initialisation**: Begin with the second element in the array (assuming the first element is already considered sorted).
2. **Insertion**: Take the next element from the unsorted part of the array and insert it into its correct position within the sorted part of the array.
3. **Incremental Sorting**: Repeat the above process for each remaining element in the unsorted part of the array until the entire array is sorted.

```
def insertion_sort(A):
	n ← size(A)
	for i in [1:n] do
		x ← A[i]
		# move forward entries > x
		j ← i
		while j > 0 and x < A[j-1] do
			A[j] ← A[j-1]
			j ← j - 1
		# if j>0 ⇒ x ≥ A[j-1]
		# if j<i ⇒ x < A[j+1]
		A[j] ← x
```

## Performance

- **Best Case**: $O(n)$ - Insertion sort performs efficiently when the input array is already sorted or nearly sorted.
- **Average Case**: $O(n^2)$ - On average, insertion sort performs $\frac{n^2}{4}$ comparisons and swaps.
- **Worst Case**: $O(n^2)$ - When the input array is in reverse order, insertion sort performs the maximum number of comparisons and shifts.

### Time Complexity

The time complexity of insertion sort is $O(n^2)$, where $n$ is the number of elements in the array.

In the worst-case scenario, when the input array is in reverse order, each element may need to be compared and shifted to its correct position within the sorted subarray. This results in a quadratic time complexity.

### Space Complexity

Insertion sort is an in-place sorting algorithm, meaning it requires only a constant amount of additional space $O(1)$ for temporary storage during element insertion.