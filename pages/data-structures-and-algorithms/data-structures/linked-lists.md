# Linked Lists

Linked list is a concrete data structure.

It contains sequence of Nodes, each with a reference to the next node

## Singly Linked Lists

List captured by reference (head) to the first Node

Each Node in a singly linked List stores
- its element, and
- a link to the next node.

### Getter Method

`first()`  return position of first element (null if empty), which is the head node.

### Insert First Method

`insertFirst(e)` inserts the value at the head node.
1. Instantiate a new node $x$
2. Set $e$ as element of $x$
3. Set $x.next$ to point to (old) head
4. Update list’s head to point to $x$

The time complexity of this method is $O(1)$.

### Remove First Method

`removeFirst()` removes the first node.
1. Update head to point to next node
2. Delete the former first node

The time complexity of this method is $O(1)$.

### Insert Before Method

`insertBefore(p,e)` inserts $e$ in front of the element at position $p$

To find the predecessor of $p$ we need to follow the links from
the “head”. 

This takes the time complexity of $O(n)$. There is no constant-time way to find the predecessor of a node in a singly linked list.

## Doubly Linked Lists

A concrete data structure
- A sequence of Nodes, each with reference to $prev$ and to $next$
- List captured by references to its Sentinel Nodes

### Insert Before Method

`insertBefore(p,e)` inserts a new node with element $e$ between $p$ and its predecessor.

1. Instantiate new Node $x$ with element set to $e$.
2. Update $x.previous$ to point to $p.previous$ and $x.next$ to point to $p$.
3. Update $p.prev.next ← x$ and $p.prev ← x$

```
def insert_before(pos, elem):
    // insert elem before pos
    // assuming it is a legal pos
    new_node ← create a new node
    new_node.element ← elem
    new_node.prev ← pos.prev
    new_node.next ← pos
    pos.prev.next ← new_node
    pos.prev ← new_node
    return new_node
```

### Remove Method

`remove(p)` removes a node, $p$, from a doubly-linked list.


```
def remove(pos):
    // remove pos from the list
    // assuming it is a legal pos
    pos.prev.next ← pos.next
    pos.next.prev ← pos.prev
    return pos.element
```

## Performance

A (doubly) linked list can perform all of the accessor and update operations for a positional list in constant time.

Space complexity is $O(n)$

Time complexity is $O(1)$ for all operations