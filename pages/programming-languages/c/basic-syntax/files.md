# Files

`FILE` is a [struct](structures.md) that is defined in stdio.h and this is the descriptor.

To open a file, we use the `fopen` function.

```c
FILE *fopen(const char *path, const char *mode);

FILE * myfile = fopen(
    "turtles.txt",      // filename or file path
    "w"                 // mode: "r", "w", "a" etc.
)
```