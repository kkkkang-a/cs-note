# Data Structures

Data structure is a format for storing, managing and working with or structuring data or information. For example, arrays and linked lists.

## Iterators

Iterators abstract the process of stepping through a collection of elements one at a time by extending the concept of position. They are implemented by maintaining a cursor to the "current" element.

There are two notions of iterators:
- Snapshot Iterator: Freezes the contents of the data structure. If we modify the collection, behavior becomes unpredictable.
- Dynamic Iterator: Follows changes to the data structure. Behavior changes predictably with modifications

## Abstract Data Types (ADTs)

Abstract Data Types (ADTs) specify desired behavior from the user's point of view. They provide a high-level description of operations that can be performed on the data without specifying how they are implemented.

A data structure, on the other hand, is a concrete representation of data from the implementer's perspective. It provides specific implementations of operations defined by the ADT.

The distinction between ADTs and data structures is subtle but akin to the difference between a computational problem and an algorithm.

- [Lists](lists.md)
    - [Arrays](arrays.md)
    - [Linked Lists](linked-lists.md)
- [Stacks](stacks.md)
- [Queues](queues.md)
	- [Priority Queues](priority-queue.md)
- [Trees](trees.md)
    - [Binary Trees](binary-trees.md)
- [Maps](maps.md)