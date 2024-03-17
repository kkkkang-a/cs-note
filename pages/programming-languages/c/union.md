# Union

C union allows the declarance of variables that occupy the same memory.

Unlike a [struct](structures.md) variable, a variable of union type, only one of its members can contain a value at any given time, whereas a struct variable stores values of all the elements.


## Syntax

The union keyword defines a new data type with more than one member for the program.

```c
union myunion{
    int a;
    double b;
    char c;
};
```

## Memory Allocation

The main difference between struct and union is the size of the variables.

For a union type variable, the compiler allocates a chunk of memory of the size enough to accommodate the element of largest byte size.

```c
union myunion{
   int a;
   double b;
   char c;
};
```
For the union above, the `myunion` type has an int, double and a char element. Out of which the size of double is the largest − 8.

However, in a similar struct variable, the compiler allocates the memory to a struct variable, to be able to store values for all the elements.

```c
struct mystruct{
   int a;
   double b;
   char c;
};
```

In `mystruct`, there are three elements one each int, double and char, requiring 13 bytes.

Using only struct variable might result in a major waste of memory.