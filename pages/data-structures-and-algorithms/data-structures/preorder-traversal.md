# Preorder Traversal

Preorder traversal is a method of traversing or visiting all the nodes in a tree in a specific order.

Preorder traversal is typically implemented recursively.

## Implementation

In preorder traversal, we start at a given node and visit that node before visiting its descendants.

Then, we recursively apply the same process to each of its child nodes in order.

Visit does some work on the node:
- print node data
- aggregate node data
- modify node data

```
def pre_order(v)
    visit(v)
    for each child w of v
        pre_order(w)
```

Nodes are numbered in the order they are visited when we call `pre_order()` starting at the root node.

## Examples

Example 1:

```
     A
    / \
   B   C
  / \
 D   E
```

The preorder traversal of this tree would visit nodes in the order: A, B, D, E, C.

Example 2:

![preorder-traversal](images/preorder-traversal.png)
