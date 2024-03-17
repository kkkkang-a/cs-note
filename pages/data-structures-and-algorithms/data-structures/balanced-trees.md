# Balanced Trees

A family of balanced BST implementations that use the idea of keeping a “rank” for every node.

This directly translates into $O(\log_2n)$ performance for searching.

Rank-balanced trees aim to reduce the discrepancy between the ranks of the left and right subtrees:
- [AVL Trees](pages/data-structures-and-algorithms/data-structures/avl-trees.md)