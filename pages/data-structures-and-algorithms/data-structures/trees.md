# Trees

A tree is a widely used abstract data type that represents a hierarchical tree structure with a set of connected nodes.

Each node in the tree can be connected to many children (depending on the type of tree), but must be connected to exactly one parent, except for the root node, which is the top-most node in the tree hierarchy.

## Definition

A tree is made up of a set of nodes endowed with parent-child relationship with following properties:
- If the tree is non-empty, it has a special node called the root that has no parent
- Every node of the treeother than the root has a unique parent
- Following the parent relation always leads to the root (i.e. the parent-child relation does not have "cycles")

## Terminology

**Root**: The node without parent node.

**Internal Node**: Any node of a tree that has child nodes.

**External/Leaf Node**: Any node that does not have child nodes.

**Ancestor**: A node reachable by repeated proceeding from child to parent. A root node will always be the ancestor of any other nodes.

**Descendant**: A node reachable by repeated proceeding from parent to child. Every node is a descendant of the root

**Sibling**: Child nodes with the same parent node.

**Depth**: The number of edges along the unique path between it and the root node.

**Level**: The set of nodes with the same depth.

**Height**: The length of the longest downward path to a leaf from that node. This is the maximum depth.

**Distance**: The number of edges along the shortest path between two nodes

**Subtree**: Each non-root node can be treated as the root node of its own subtree, which includes that node and all its descendants.

**Edge**: A pair of nodes such that one is the parent of the other.

**Path**: Sequence of nodes such that 2 consecutive nodes in the sequence have an edge.

**Ordered Tree**: In an ordered tree, there is a prescribed order for each node’s children.

## Operations

The Position represents an abstract object that refers to a specific element within the tree. It could be a node or any other suitable representation depending on the implementation.

Generic Methods:
- `size()`: Returns the total number of elements/nodes in the tree.
- `isEmpty()`: Checks if the tree is empty or not.
- `iterator()`: Returns an iterator over all the elements in the tree.
- `positions()`: Returns an iterable collection of all positions (nodes) in the tree.

Access Methods:
- `root()`: Returns the position of the root node of the tree.
- `parent(p)`: Returns the parent position of the node `p`.
- `children(p)`: Returns an iterable collection of positions representing the children of the node `p`.
- `numChildren(p)`: Returns the number of children of the node `p`.

Query Methods:
- `isInternal(p)`: Checks if the node `p` is an internal node (has at least one child).
- `isExternal(p)`: Checks if the node `p` is an external node (a leaf node with no children).
- `isRoot(p)`: Checks if the node `p` is the root of the tree.

Node Object Implementation:
- `value`: Represents the value associated with the node.
- `children`: Represents the children of the node, typically stored as a set or list.
- `parent`: Represents the parent node of the current node. This attribute may be optional depending on the implementation.

```
def is_external(v)
    # test if v is a leaf
    return v.children.is_empty()

def is_root(v)
    # test if v is the root
    return v.parent = null
```

## Traversing Trees

A traversal visits the nodes of a tree in a systematic manner.

When traversing a simpler structure like a list there is one natural traversal strategy (forward or backwards)

[Eular tour traversal](pages/data-structures-and-algorithms/data-structures/euler-tour-traserval.md) is gaeneric traversal of a binary tree.

Trees are more complex and admit more than one natural way:
- [pre-order](pages/data-structures-and-algorithms/data-structures/preorder-traversal.md)
- [post-order](pages/data-structures-and-algorithms/data-structures/postorder-traversal.md)
- [in-order](pages/data-structures-and-algorithms/data-structures/binary-trees.md#inorder-traversal) (for [binary trees](pages/data-structures-and-algorithms/data-structures/binary-trees.md))