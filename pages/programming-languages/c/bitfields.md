# Bit Fields

Bit fields are good for low level programming of device registers (drivers, embedded systems etc) and “unpacking” data structures.

It can specify a size, in bits, for elements of a structure. The size is placed after the field name, with a colon between:

```c
struct IOdev {
    unsigned R_W: 1;
    unsigned Dirn: 8;
    unsigned mode: 3;
};
```

## Bit Operations

- shift right: `>>`
- shift left: `<<`
- bitwiseAND: `&`
- bitwise OR: `|`
- bitwise XOR: `^`
- bitwise NOT: `~`