# free()

The `free()` is used to de-allocate memory previously allocated by any of the memory allocation functions.

Memory allocated by the `malloc()` and `calloc()` functions must be manually de-allocated when not in use. Freeing it helps to reduce memory wastage.  

## Syntax

```c
#include <stdlib.h>
void free(void *ptr);
```

The `memoryblock` must exist beforehand in order to be de-allocated by the `free()` function.

## Example

```c
int * ptr;  
ptr = (int *)malloc(sizeof(int)*20);
// ptr = starting address of the 20 integers

free((void *)ptr);
// ptr = NULL;
```