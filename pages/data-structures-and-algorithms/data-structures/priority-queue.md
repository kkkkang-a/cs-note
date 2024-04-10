# Priority Queues

A priority queue is a special type of Abstract Data Type (ADT) used to store a collection of key-value items, where the main operation is to remove the item with the smallest key.

- `insert(k, v)`: Insert an item with key `k` and value `v` into the priority queue.
- `remove_min()`: Remove and return the item with the smallest key from the priority queue.
- `min()`: Return the item with the smallest key without removing it from the priority queue.
- `size()`: Return the number of items stored in the priority queue.
- `is_empty()`: Test if the priority queue is empty.

Priority queues are commonly used in applications such as stock matching engines, task scheduling, and network routing algorithms.

## Sequence-Based Priority Queue

The priority queue can be implemented using a sequence (e.g., list or array), which can be either sorted or unsorted.

### Unsorted List Implementation

- `insert`: $O(1)$ time complexity since we can insert the item at the beginning or end of the sequence.
- `remove_min` and `min`: $O(n)$ time complexity since we have to traverse the entire list to find the smallest key.

### Sorted List Implementation

- `insert`: $O(n)$ time complexity since we have to find the place where to insert the item.
- `remove_min` and `min`: $O(1)$ time complexity since the smallest key is at the beginning.

To sort the list, [insertion sort](../algorithms/insertion-sort.md) or [selection sort](../algorithms/selection-sort.md) can be used.

## Heap-Based Priority Queue

A more efficient implementation of a priority queue can be achieved using a [binary heap](heaps.md).

- A binary heap is a complete binary tree where the key at each node is greater than or equal to the keys of its children (max-heap) or less than or equal to the keys of its children (min-heap).
- In a max-heap, the item with the largest key is stored at the root.
- In a min-heap, the item with the smallest key is stored at the root.

The time complexity of a heap-based priority queue is always $O(n \log n)$.