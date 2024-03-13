# Binary Trees

A binary tree is a tree data structure in which each node has at most two children, referred to as the left child and the right child.

A binary tree is an ordered tree with the following properties:
- Each internal node has at most two children
- Each child node is labeled as a left child or a right child
- Child ordering is left followed by right

We say the binary tree is proper if every internal node has two children.

## Types of Binary Trees

- [Binary Search Trees](./binary-search-trees.md)
- [Balanced Trees](./balanced-trees.md)
    - [AVL Trees](./avl-trees.md)

## Operations

A binary tree extends the [Tree operations](./trees.md#operations).

Additional methods:
- `leftChild(p)`: Returns the left child of a given node position `p`.
- `rightChild(p)`: Returns the right child of a given node position `p`.
- `sibling(p)`: Returns the sibling of a given node position `p`.

Node object implementation typically has the following attributes:
- value: the value associated with this Node
- left: left child of this Node
- right: right child of this Node
- parent: (optional) the parent of this Node

```
def is_external(v)
    # test if v is a leaf
    return v.left = null and v.right = null
```

## Traversing Binary Trees

[Eular tour traversal](./euler-tour-traserval.md) is gaeneric traversal of a binary tree.

### Inorder Traversal

To do an inorder traversal starting at a given node, the node is visited after its left subtree but before its right subtree.

Visit does some work on the node:
- print node data
- aggregate node data
- modify node data

```
def in_order(v)
    if v.left ≠ null then
        in_order(v.left)
    visit(v)
    if v.right ≠ null then
        in_order(v.right)
```

## Complexity of Recursive Algorithms

The complexity of recursive algorithms depends on the pattern of recursion:

- **Linear Recursion**: If a method calls itself on all children, the total cost is linear in the number of nodes.
- **Height Recursion**: If a method calls itself on at most one child, the total cost is linear in the height of the tree.

## Applications

**Arithmetic Expression Tree**: In arithmetic expression trees, internal nodes represent operators, and external nodes represent operands. These trees are used to represent mathematical expressions and evaluate them efficiently.
- internal nodes: operators
- external nodes: operands

**Decision Trees**: Decision trees are a powerful tool in machine learning and decision-making processes. In a decision tree, internal nodes represent questions with yes/no answers, and external nodes represent decisions or outcomes. They're used in classification and regression tasks.
- internal nodes: questions with yes/no answer
- external nodes: decisions