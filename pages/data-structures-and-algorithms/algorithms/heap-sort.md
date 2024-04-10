# Heap Sort

Heap sort is a comparison-based sorting algorithm that leverages the [heap data structure](../data-structures/heaps.md) to efficiently sort elements in ascending or descending order.

## Algorithm Overview:

1. **Heapify the Array**: Convert the input array into a max-heap or min-heap, depending on whether you want to sort in ascending or descending order.
2. **Sorting Phase**:
   - For each element in the heap:
     - Swap the root element (maximum for max-heap, minimum for min-heap) with the last element in the heap.
     - Reduce the heap size by one.
     - Restore the heap property (heapify) on the reduced heap.
3. **Final Array**: After the sorting phase, the array will be sorted in ascending order if using a max-heap or descending order if using a min-heap.

## Performance

There is no worst-case scenarios as it always has a time complexity of $O(n \log n)$.

### Time Complexity

- **Building the Heap**: $O(n)$ - Building a heap from an array of n elements takes linear time.
- **Sorting Phase**: $O(n \log n)$ - For each element, swapping and heapifying takes logarithmic time. Since there are n elements, the overall time complexity is O(n log n).

### Space Complexity

Heap sort is an in-place sorting algorithm, meaning it doesn't require additional memory proportional to the input size.

However, it may require a constant amount of extra space for temporary variables during sorting.
