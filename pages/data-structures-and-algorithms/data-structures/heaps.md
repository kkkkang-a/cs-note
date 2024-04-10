# Heaps

A heap is a [binary tree](binary-trees.md) storing (key, value) items at its nodes, satisfying the following properties:
1. **Heap-Order**: for every node $m \neq root, key(m) \gt key(parent(m))$
2. **Complete Binary Tree**

A heap storing $n$ keys has height $\log n$

## Operations

### Insertion into a Heap

**Time Complexity:** $O(\log n)$ - The height of the heap determines the number of comparisons and swaps required, which is logarithmic with respect to the number of elements in the heap.

#### Min-Heap

To insert a new element into a min-heap:
1. Place the new element at the bottom level of the heap.
2. Compare the new element with its parent.
3. If the new element is smaller than its parent, swap them.
4. Repeat steps 2-3 until the heap property is restored.

#### Max-Heap

To insert a new element into a max-heap:
1. Place the new element at the bottom level of the heap.
2. Compare the new element with its parent.
3. If the new element is greater than its parent, swap them.
4. Repeat steps 2-3 until the heap property is restored.

### Removal from a Heap

**Time Complexity:** $O(\log n)$ - The number of comparisons and swaps required to restore the heap property is logarithmic with respect to the number of elements in the heap.

#### Min-Heap

To remove the minimum element from a min-heap:
1. Replace the root of the heap with the last element.
2. Remove the last element from the heap.
3. Restore the heap property by moving the new root down the tree, swapping it with its smallest child until the heap property is restored.

#### Max-Heap

To remove the maximum element from a max-heap:
1. Replace the root of the heap with the last element.
2. Remove the last element from the heap.
3. Restore the heap property by moving the new root down the tree, swapping it with its largest child until the heap property is restored.
