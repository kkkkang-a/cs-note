# Binary Search Trees

A binary search tree is a binary tree storing keys (or key-value pairs) satisfying the following BST property:

For any node `v` in the tree and any node `u` in the left subtree of `v` and any node `w` in the right subtree of `v`:

$$
key(u) \lt key(v) \lt key(w)
$$

## Implementation

> [!NOTE]
> To simplify the presentation of our algorithms, we only store keys (or key-value pairs) at internal nodes. External nodes do not store items but `null`.

To search for a key `k`, we trace a downward path starting at the root.

To decide whether to go left or right, we compare the key of the current node `v` with `k`.

If we reach an external node, this means that the key is not in the data structure.

```
def search(k, v)
    if v.isExternal() then
        # unsuccessful search
        return v
    if k = key(v) then
        # successful search
        return v
    else if k < key(v) then
        # recurse on left subtree
        return search(k, v.left)
    else
        # that is k > key(v)
        # recurse on right subtree
        return search(k, v.right)
```

## Operation

### Insertion

To perform operation `put(k, o)`, we search for key `k` (using search).

If `k` is found in the tree, replace the corresponding value by `o`.

If `k` is not found, let `w` be the external node reached by the search. We replace `w` with an internal node holding `(k, o)`.

### Deletion

To perform operation `remove(k)`, we search for key `k` (using search) to find the node `w` holding `k`.

If `k` is not in the tree we can either throw an exception or do nothing depending on the ADT specs.

If `w` is found in the tree, we distinguish between two cases:
1. `w` has one internal child and one external child
2. `w` has two internal children

#### Case 1: One Internal Child, 1 External Child

Suppose that the node `w` we want to remove has an external child, which we call `z`.

To remove `w`:
1. remove `w` and `z` from the tree
2. promote the other child of `w` to take `w`'s place

```
before removal of 8:
       5
      / \
     3   8
    / \   \
   2   4   9

after removal of 8:
       5
      / \
     3   9
    / \  
   2   4 
```

#### Case 2: Two Internal Children

Suppose that the node `w` we want to remove has two internal children.

To remove `w`:
1. find the internal node `y` following `w` in an inorder traversal (i.e., `y` has the smallest key among the right subtree under `w`)
2. we copy the entry from `y` into node `w`
3. we remove node `y` and its left child `z`, which must be external, using previous case

```
before removal of 3:
       5
      / \
     3   8
    / \ / \
   2  4 7  9

after removal of 3:
       5
      / \
     4   8
    /   / \
   2   7   9
```

#### Deletion Algorithm

```
def remove(k)
    w ← search(k, root)
    if w.isExternal() then
        # key not found
        return null
    else if w has at least one external child z then
        remove z
        promote the other child of w to take w’s place
        remove w
    else
        # y is leftmost internal node in the right subtree of w
        # y is the next node of k in the inorder traversal
        y <- immediate successor of w
        replace contents of w with entry from y
        remove y as above
```

### Range Queries

A range query is defined by two values `k1` and `k2`. We are to find all keys `k` stored in `T` such that $$k_1 \leq k \leq k_2$.

The algorithm is a restricted version of inorder traversal. When at node `v`:
- if $key(v) \lt k_1$: Recursively search right subtree
- if $k_1 \leq key(v) \leq k_2$: Recursively search left subtree, add v to range output, search right subtree
- if $k_2 \lt key(v)$: Recursively search left subtree

```
def range_search(T, k1, k2)
    output ← []
    range(T.root, k1, k2)

def range(v, k1, k2)
    if v is external then
        return null
    if key(v) > k2 then
        range(v.left, k1, k2)
    else if key(v) < k1 then
        range(v.right, k1, k2)
    else
        range(v.left, k1, k2)
        output.append(v)
        range(v.right, k1, k2)
```

## Performance

Consider a binary search tree with $n$ items and height $h$:
- the space used is $O(n)$
- get, put and remove take $O(h)$ time

The height $h$ can be $n$ in the worst case and $\log_2n$ in the best case.

## Duplicate Keys

In a standard BST, duplicates are not allowed.

It is possible to change it to allow duplicates. But that means additional complexity in the BST implementation:
- Allowing left descendants to be equal to the parent
    $$key(left descendant) ≤ key(node) < key(right descendant)$$
- Using a list to store duplicates

The time complexity for insertion and deletion would still be $O(h)$, where $h$ is the height of the tree.

It might increase the complexity of the operation slightly as it may require additional comparisons to determine the placement of duplicates.