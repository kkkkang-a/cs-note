# Functions

A function is a block of code which only runs when it is called.

Functions are used to perform certain actions, and they are important for reusing code: Define the code once, and use it many times.

## Sharing Data in Function Calls

Passing data to functions typically involves either passing the data by value or by reference.

When passing data by value, a copy of the data is made and passed to the function, while passing by reference allows the function to directly manipulate the original data. 

### Passing by Value

Passing by value involves making a copy of the data and passing it to the function.

This approach is simple and straightforward, but it can be inefficient for large data structures as it requires memory allocation for the copy.

```c
void increment(int x) {
    x++; // Changes local copy of x, not the original
}

int main() {
    int num = 5;
    increment(num); // num remains 5
    return 0;
}
```

### Passing by Reference (Using Pointers)

Passing by reference is achieved by passing the address of the data to the function, typically using pointers.

This allows the function to directly access and modify the original data, avoiding the overhead of copying large data structures.

```c
void increment(int *x) {
    (*x)++; // Changes the value at the memory location pointed to by x
}

int main() {
    int num = 5;
    increment(&num); // num becomes 6
    return 0;
}
```

### Benefits of Passing by Reference with Pointers

1. **Efficiency**: Passing by reference with pointers avoids unnecessary copying of data, making it more efficient, especially for large data structures.
2. **Mutable Data**: Functions can modify the original data, enabling more flexible and powerful functionality.
3. **Indirection**: Pointers allow indirect access to data, enabling dynamic memory management and complex data structures.
4. **Shared State**: By passing pointers, multiple functions can operate on the same data, facilitating communication and collaboration between different parts of a program.
