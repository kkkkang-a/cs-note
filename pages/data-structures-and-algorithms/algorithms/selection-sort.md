# Selection Sort

Selection sort is a simple sorting algorithm that repeatedly selects the minimum element from the unsorted portion of the array and moves it to the beginning.

The algorithm divides the input array into two parts: the sorted subarray which is built up from left to right at the front of the array, and the unsorted subarray containing the remaining elements yet to be sorted.

## Algorithm

1. **Initialisation**: Begin with the entire array considered as unsorted.
2. **Selection**: Find the minimum element from the unsorted subarray and swap it with the element at the beginning of the unsorted subarray.
3. **Incremental Sorting**: Repeat the above process for the remaining unsorted subarray until the entire array is sorted.

```
def selection_sort(A):
	n ← size(A)
	for i in [0:n] do
	# find s ⩾ i minimizing A[s]
	s ← i
	for j in [i:n] do
		if A[j] < A[s] then
			s ← j
	# swap A[i] and A[s]
	A[i], A[s] ← A[s], A[i]
```

## Performance

- **Best Case**: $O(n^2)$ - Even if the input array is already sorted, the algorithm still iterates over the entire array to find the minimum element in each pass.
- **Average Case**: $O(n^2)$ - On average, the algorithm performs $\frac{n^2}{2}$ comparisons and swaps.
- **Worst Case**: $O(n^2)$ - When the input array is sorted in reverse order, selection sort performs the maximum number of comparisons and swaps.

### Time Complexity

The time complexity of selection sort is $O(n^2),$ where n is the number of elements in the array.

- **Selection of Minimum**: Finding the minimum element in the unsorted subarray requires scanning through the unsorted portion, which takes $O(n)$ time in the worst case.
- **Swapping**: After finding the minimum element, swapping it with the first element of the unsorted subarray takes constant time.
- **Iterations**: Since the selection process is repeated $n$ times (once for each element), the total time complexity is $O(n^2)$.

### Space Complexity

Selection sort is an in-place sorting algorithm, meaning it requires only a constant amount of additional space $O(1)$ for temporary storage during swapping operations.