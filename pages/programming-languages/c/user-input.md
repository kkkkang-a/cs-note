# User Input

To get user input, you can use the `scanf()` function.

The `scanf()` function takes two arguments:
1. the format specifier of the variable
2. the reference operator which stores the [memory address](./c-memory-address.md) of the variable.

```c
// Create an integer variable that will store the number we get from the user
int myNum;

// Get and save the number the user types
scanf("%d", &myNum);
```

The `scanf()` function has some limitations: it considers space (whitespace, tabs, etc) as a terminating character, which means that it can only display a single word.

`fgets()` function is often used to read a line of text.

The `fgets()` function takes three arguments:
1. the name of the string variable
2. sizeof(string_name)
3. stdin

```c
char fullName[30];

printf("Type your full name: \n");
fgets(fullName, sizeof(fullName), stdin);

printf("Hello %s", fullName);

// Type your full name: John Doe
// Hello John Doe
```