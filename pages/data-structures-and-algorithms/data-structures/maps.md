# Maps

The map is an abstract data type that contains a collection of records. 

It stores a collection of key-value pairs, such that each possible key appears at most once in the collection.

## Operations

Maps support 'lookup', 'remove', and 'insert' operations.

- `get(k)`: if the map M has an entry with key k, return its associated value
- `put(k, v)`: if key k is not in M, then insert (k, v) into the map M; else, replace the existing value associated to k with v
- `remove(k)`: if the map M has an entry with key k, remove it
- `size()`, `isEmpty()`
- `entrySet()`: return an iterable collection of the entries in M
- `keySet()`: return an iterable collection of the keys in M
- `values()`: return an iterable collection of the values in M

If a map is sorted, it supports more operations.

- `firstEntry()` returns the entry with smallest key; if map is empty, returns null
- `lastEntry()` returns the entry with largest key; if map is empty, returns null
- `ceilingEntry(k)` returns the entry with least key that is greater than or equal to `k` (or null, if no such entry exists)
- `floorEntry(k)` returns the entry with greatest key that is less than or equal to `k` (or null, if no such entry exists)
- `lowerEntry(k)` returns the entry with greatest key that is strictly less than `k` (or null, if no such entry exists)
- `higherEntry(k)` returns the entry with least key that is strictly greater than `k` (or null, if no such entry exists)
- `subMap(k1, k2)` returns an iteration of all the entries with key greater than or equal to `k1` and strictly less than `k2`

## Implementation

### List-Based (Unsorted) Map

We can implement a map using an unsorted [list](pages/data-structures-and-algorithms/data-structures/lists.md) of key-item pairs

To do a get and put we may have to traverse the whole list, so those operations take $O(n)$ time.

Only feasible if map is very small or if we put things at the end and do not need to perform many gets (i.e., system log).

![list-based-map](images/list-based-map.png)

### Tree-Based (Sorted) Map

We can implement a sorted map using an [AVL tree](pages/data-structures-and-algorithms/data-structures/avl-trees.md), where each node stores a key-item pair.

To do a get or a put we search for the key in the tree, so these operations take $O(h)$ time, which can be $O(\log_2n)$ if the tree is balanced.

Only feasible if there is a total ordering on the keys.