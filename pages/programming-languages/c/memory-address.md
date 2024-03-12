# Memory Address

When a variable is created in C, a memory address is assigned to the variable.

The memory address is the location of where the variable is stored on the computer.

When we assign a value to the variable, it is stored in this memory address.

The address operator `&` is used to access the address of a variable.

```c
int myAge = 43;
printf("%p", &myAge); // Outputs 0x7ffe5367e044
```

The memory address is in hexadecimal form (0x..). You will probably not get the same result in your program, as this depends on where the variable is stored on your computer.

`&myAge` is often called a [pointer](./pointers.md). A pointer basically stores the memory address of a variable as its value. To print pointer values, we use the `%p` format specifier.

An example of the the address operator in action is to receive an integer from standard input.

```c
int age;
scanf("%d", &age);
```