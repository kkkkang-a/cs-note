# C Basic Data Types

A variable in C must be a specified data type, and you must use a format specifier inside the printf() function to display it.

The data type specifies the size and type of information the variable will store.

| Data Type | Size      | Description                                       | Format Specifier |
|-----------|-----------|---------------------------------------------------|------------------|
| `int`       | 2 or 4 bytes | Stores whole numbers, without decimals           | %d               |
| `float`     | 4 bytes     | Stores fractional numbers, containing one or more decimals. Sufficient for storing 6-7 decimal digits | %f               |
| `double`    | 8 bytes     | Stores fractional numbers, containing one or more decimals. Sufficient for storing 15 decimal digits | %lf              |
| `char`      | 1 byte      | Stores a single character/letter/number, or ASCII values | %c               |

Not all hardware architectures are the same - different sizes for basic types.

C specification does not dictate exactly how many bytes an int will be.

`sizeof` operator returns the number of bytes used to represent the given type or expression.

## Characters

The char data type is used to store a single character.

ASCII values can be used to display certain characters. Note that these values are not surrounded by quotes (''), as they are numbers:

```c
char a = 65, b = 66, c = 67;    // ASCII code for a, b, c
printf("%c", a);
printf("%c", b);
printf("%c", c);
```

The types char will support the value range from `CHAR_MIN` to `CHAR_MAX` as defined in file <limits.h>

```c
#define UCHAR_MAX 255     // max value for an unsigned char
#define CHAR_MAX 127      // max value for a char
#define CHAR_MIN (-128)   // min value for a char
```

## Decimal Precision

If you want to remove the extra zeros (set decimal precision), you can use a dot (.) followed by a number that specifies how many digits that should be shown after the decimal point:

```c
float myFloatNum = 3.5;

printf("%f\n", myFloatNum);   // Default will show 6 digits after the decimal point
printf("%.1f\n", myFloatNum); // Only show 1 digit
printf("%.2f\n", myFloatNum); // Only show 2 digits
printf("%.4f", myFloatNum);   // Only show 4 digits
```