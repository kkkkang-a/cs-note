# Lists

## Sequential (Index-Based) Lists

A data structure is said to have sequential access if one can only visit the values it contains in one particular order.

A sequential list (usually) supports the following operations:

- `size()` (int) number of elements in the store
- `isEmpty()` (boolean) whether or not the store is empty
- `get(i)` return element at index i
- `set(i, e)` replace element at index i with element e, and return element that was replaced
- `add(i, e)` insert element e at index i existing elements with index ≥ i are shifted up
- `remove(i)` remove and return the element at index i existing elements with index ≥ i are shifted down

One example of the sequential list is the [array](./arrays.md).

## Positional Lists

ADT for a list where we store elements at “positions”.

Position models the abstract notion of place where a single object is stored within a container data structure.

Unlike index, this keeps referring to the same entry even after insertion/deletion happens elsewhere in the collection.

Position offers just one method:
- `element()` return the element stored at the position instance

A positional list (usually) supports the following operations:
- `size()` (int) number of elements in the store
- `isEmpty()` (boolean) whether or not the store is empty
- `first()` return position of first element (null if empty)
- `last()` return position of last element (null if empty)
- `before(p)` return position immediately before p (null if p is first)
- `after(p)` return position immediately after p (null if p last)
- `insertBefore(p, e)` insert e in front of the element at position p
- `insertAfter(p, e)` insert e following the element at position p
- `remove(p)` remove and return the element at position p

One example of the positional list is the [linked list](./linked-lists.md).

## Comparesion Between Array and Linked List

Arrays:
- good match to index-based ADT
- caching makes traversal fast in practice
- no extra memory needed to store pointers
- allow random access (retrieve element by index)

Linked Lists:
- good match to positional ADT
- efficient insertion and deletion
- simpler behaviour as collection grows
- modifications can be made as collection iterated over
- space not wasted by list not having maximum capacity