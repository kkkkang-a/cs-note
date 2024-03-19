# realloc()

The `realloc()` function is used to reallocate a block of memory.

If the memory that was previously allocated using the `malloc()` or `calloc()` function is not sufficient, it can be reallocated using the `realloc()` function.  

## Syntax

```c
#include <stdlib.h>  
void *realloc(void *ptr, size_t size);
```

The `*ptr` or the memory block must exist beforehand. The `size` is of type `size_t`

This takes previously-allocated memory and attempts to resize it.

This may require a new block of memory to be found, so it returns a new void pointer to memory.

Contents are preserved.

## Example

```c
int *ptr;

// Memory allocated using malloc() function
ptr = (int*) malloc(5 * sizeof(int));

// ptr is reallocated with 40 bytes (4 * 10) of memory
ptr = realloc(ptr, 10 * sizeof(int));
```