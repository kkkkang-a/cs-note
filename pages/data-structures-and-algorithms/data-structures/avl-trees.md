# AVL Trees

An AVL tree is a self-balancing binary search tree.

In an AVL tree, the heights of the two child subtrees of any node differ by at most one.

If at any time they differ by more than one, rebalancing is done to restore this property. 

## Definition

AVL trees are rank-balanced trees, where `r(v)` is its height of the subtree rooted at `v`.

Balance constraint: The ranks of the two children of every internal node differ by at most 1.

The height of an AVL tree storing n keys is $O(\log_2n)$.

> [!NOTE]
> Proof (by induction):
> 
> Let $N(h)$ be the minimum number of keys of an AVL tree of height $h$.
> - We easily see that $N(1) = 1$ and $N(2) = 2$.
> - Clearly $N(h) > N(h-1)$ for any $h \geq 2$.
> - For $h > 2$, the smallest AVL tree of height $h$ contains the root node,
>   one AVL subtree of height $h-1$, and another of height at least $h-2$:
>   $$N(h) \geq 1 + N(h-1) + N(h-2) > 2N(h-2)$$
> - By induction, we can show that for $h$ even $N(h) \geq 2^{\frac{h}{2}}$.
> - Taking logarithms: $h < 2 \log N(h)$.
>
> Thus, the height of an AVL tree is $O(\log n)$.

## Operation

### Insertion

Suppose we are to insert a key `k` into our tree:

1. If `k` is in the tree, search for `k` ends at node holding `k`. There is nothing to do so tree structure does not change
2. If `k` is not in the tree, search for `k` ends at external node `w`. Make this be a new internal node containing key `k`
3. The new tree has BST property, but it may not have AVL balance property at some ancestor of `w` since
    - some ancestors of `w` may have increased their height by 1
    - every node that is not an ancestor of `w` hasn’t changed its height
4. We use rotations to re-arrange tree to re-establish AVL property, while keeping BST property

### Removal

Suppose we are to remove a key `k` from our tree:

1. If `k` is not in the tree, search for `k` ends at external node
There is nothing to do so tree structure does not change
2. If `k` is in the tree, search for `k` performs usual BST removal
leading to removing a node with an external child and
promoting its other child, which we call `w`
3. The new tree has BST property, but it may not have AVL
balance property at some ancestor of `w` since
    - some ancestors of `w` may have decreased their height by 1
    - every node that is not an ancestor of `w` hasn’t changed its heights
4. We use rotations to rearrange tree and re-establish AVL
property, while keeping BST property

## Rebalancing

During a modifying operation the height difference between two child subtrees changes, this may, as long as it is < 2, be reflected by an adaption of the balance information at the parent.

### Single Rotation

Let `x`, `y`, `z` be nodes such that `x` is a child of `y` and `y` is a child of `z`.

Let `a`, `b`, `c` be the inorder listing of `x`, `y`, `z`

Perform the rotations so as to make `b` the topmost node of the three.

![single-rotation](/images/single-rotation.png)

### Double Rotation

Let `x`, `y`, `z` be nodes such that `x` is a child of `y` and `y` is a child of `z`.

Let `a`, `b`, `c` be the inorder listing of `x`, `y`, `z`

Perform the rotations so as to make `b` the topmost node of the three.

![double-rotation](/images/double-rotation.png)

## Performance

Suppose we have an AVL tree storing n items then
- The data structure uses $O(n)$ space
- Height of the tree $O(\log_2n)$
- Searching takes $O(\log_2n)$ time
- Insertion takes $O(\log_2n)$ time
- Removal takes $O(\log_2n)$ time

A single or double rotation takes $O(1)$ time, because it involves updating $O(1)$ pointers.