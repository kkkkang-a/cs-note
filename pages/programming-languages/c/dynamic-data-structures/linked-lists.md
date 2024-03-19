# Linked Lists

A [linked-list](../../../data-structures-and-algorithms/data-structures/linked-lists.md) is an abstract data structure.

In C, the word “linked” hints at [pointers](../basic-syntax/pointers.md) to where the next element in the list is located.

Linked lists are different from [arrays](../basic-syntax/arrays.md), which use contiguous memory locations. Linked lists may use multiple links to link elements according to different interpretations of order.

The dynamic nature of the linked list data structure means we must allocate and free memory on demand.

## Implementation

```c
struct node {
	void *data;  
	struct node *next;
};
```

Each element in our singly-linked list has two components:
- the data component
- the link component: a pointer to the next node, or `NULL` for the end of the list



