# C Arrays

Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value.

## Creating Arrays

To create an array, define the data type (like int) and specify the name of the array followed by square brackets [].

To insert values to it, use a comma-separated list, inside curly braces:

```c
int myNumbers[] = {25, 50, 75, 100};
```

Another common way to create arrays, is to specify the size of the array, and add elements later.

You are not able to change the size of the array after creation

```c
// Declare an array of four integers:
int myNumbers[4];

// Add elements
myNumbers[0] = 25;
myNumbers[1] = 50;
myNumbers[2] = 75;
myNumbers[3] = 100;
```