# Arrays

An option for implementing the list ADT is to use an array A, where $A[i]$ stores (a reference to) the element with index $i$.

If array has size $N$ then we can represent lists of size $n ≤ N$.

Limitation: can represent lists up to the capacity of the array ($n$ vs $N$)

Space complexity:
- space used is $O(N)$, whereas we would like it to be $O(n)$

Time complexity:
- both get and set take $O(1)$ time
- both add and remove take $O(n)$ time in the worst case

## Getter and Setter Methods

The `get(i)` and `set(i, e)` methods are easy to implement by accessing $A[i]$.

Must check that $i$ is a legitimate index ($0 ≤ i < n$).

Time complexity of this operation is $O(1)$ time, independent of the size of the array ($N$) or the represented list ($n$)


```
def get(i):
    # input: index i
    # output: ith element in list
    if i < 0 or i ≥ n then
        return “index out of bound”
    else
        return A[i]
```

```
def set(i, e):
    # input: index i and value e
    # do: update ith element in list to e
    if i < 0 or i ≥ n then
        return “index out of bound”
    result ← A[i]
    A[i] ← e
    return result
```

## Add Method

In an operation add(i, e), we must make room for the new element by shifting forward $n - i$ elements $A[i], …, A[n - 1]$.

Must check that there is space ($n < N$)

Time complexity is $O(n)$ in the worst case when all the elements have to move.


```
def add(i, e):
    if n = N then
        return “array is full”
    if i < n then
        for j in [n-1, n-2, … , i] do
            A[j + 1] ← A[j]
    A[i] ← e
    n ← n + 1
```

## Remove Method

In an operation remove(i), we need to fill the hole left at position $i$ by shifting backward $n - i - 1$ elements $A[i + 1], …, A[n - 1]$.

Must check that $i$ is a legitimate index ($0 ≤ i < n$).


```
def remove(i):
    if i < 0 or i ≥ n
        return “index out of bound”
    e ← A[i]
    if i < n-1
        for j in [i, i+1, … , n-2] do
            A[j] ← A[j+1]
    n ← n - 1
    return e
```

Time complexity is $O(n)$ in the worst case.