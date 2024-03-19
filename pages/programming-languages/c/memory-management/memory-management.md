# Memory Management

Memory is a long array of 8 bit pieces called bytes. Memory can be represented as an array, where the index is a [memory address](memory-address.md).

The memory allocation can be done either before or at the time of program implementation. There are two techniques for memory allocation: static memory allocation and dynamic memory allocation.

## Static Memory Allocation

In this type of allocation, the compiler allocates a fixed amount of memory during compile time and the operating system internally uses a data structure known as stack to manage the memory.

Exact memory requirements must be known in advance as once memory is allocated it can not be changed.

```c
int days;                   // Initialized or assigned some value at run time
int snowfall = 0;           // Normal variable
const int maxScore = 10;    // Constant, can not be changed
```

## Dynamic Memory Allocation

In this type of allocation, system memory is managed at runtime.

Dynamic memory management in C programming language is performed using the functions:
- [`malloc()`](malloc.md)
- [`calloc()`](calloc.md)
- [`realloc()`](realloc.md)
- [`free()`](free.md)

These four functions are defined in the `<stdlib.h>` C standard library header file. It uses the heap space of the system memory.

## Safety Issues

**Caution 1**: De-allocate memory that is no longer required.
- While the system should de-allocate resources on termination, it is good practice to take control of this process.
- In some Java programs there is a noticeable performance dip when the automatic “garbage collection” functionality kicks in.

**Caution 2**: Never attempt to de-allocate memory that has not been allocated.
- A common error is to try to free memory that has already been de-allocated, or was never allocated in the first instance.

**Caution 3**: Never try to use memory that has been de-allocated.

**Caution 4**: Know the memory allocation requirements before allocation.
- Use of the sizeof operator addresses the more obvious problems.
- A common problem is to forget that a string includes a `\0` terminating character.