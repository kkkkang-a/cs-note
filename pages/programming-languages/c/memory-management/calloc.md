# calloc()

The `calloc()` function is used to dynamically allocate an array of memory blocks of a specified type.

Each block has a default value of 0.

## Syntax

```c
#include <stdlib.h>  
void *calloc(size_t num, size_t size);
```

Both `numberofblocks` and `size` are of type `size_t`.

This is similar to [malloc](malloc.md) except that:
- It has two arguments:
	1. `num` specifies the number of “blocks” of contiguous memory
	2. `size` specifies the size of each block  
- The allocated memory is cleared (set to ‘0’).

## Example

```c
int *ptr;

// The pointer ptr holds the address of the first byte in the allocated memory
ptr = (int*) calloc(5, sizeof(int));
```

The above statement allocates contiguous space in memory for 5 elements each with the size of the `int`.