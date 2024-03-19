# malloc()

The `malloc()` function is used to allocate a block of memory in the heap. It allocates the user a specified number of bytes but does not initialise.

Once allocated, the program accesses this block of memory via a [pointer](../basic-syntax/pointers.md) that `malloc()` returns. 

## Syntax

```c
#include <stdlib.h>
void *malloc(size_t size);
```

The `size` parameter is of type `size_t`.

The default pointer returned by `malloc()` is of the type `void` but can be cast into a pointer of any data type.

However, if the space is insufficient for the amount of memory requested by `malloc()`, then the allocation fails and a `NULL` pointer is returned.

## Example

```c
int * ptr;  
ptr = (int *)malloc(sizeof(int)*20);
```

If an `int` is 4 bytes, then this call will request 80 bytes of memory from the heap.