# Structures

Structures (also called structs) are a way to group several related variables into one place. Each variable in the structure is known as a member of the structure.

Unlike an [array](pages/programming-languages/c/arrays.md), a structure can contain many different data types (int, float, char, etc.).

## Syntax

```c
struct date {               // Structure declaration
    enum day_name day;      // Member (enum)
    int day_num;            // Member (int)
    enum month_name month;  // Member (enum)
    int year;               // Member (int)
};
```

To access the structure, you must create a variable of it.

```c
// Creating a struct variable but with no data being filled.
struct date moonlanding;

// Declear and initialise a new struct variable with data.
struct date deadline = {Monday, 1, Jan, 2000};

// Declear a struct that is referenced by a pointer.
struct date *ptr_to_struct;
```

To access members of a structure, use the dot syntax or arrow (->).

```c
struct date bigday;
struct date * mydate;
int theyear;

// Directly accessing the value.
theyear = bigday.year;

// Accessing the value by creating a pointer to the structure.
mydate = &bigday;
theyear = mydate->year;     // The -> operator indicates the element required.

// Tricky notations:
theyear = mydate.year;      // Invalid, as mydate is a pointer.
theyear = (*mydate).year;   // Valid, it dereference the mydate pointer.
theyear = *mydate.year;     // Valid, the bracket can be ignored.
theyear = *(mydate.year);   // Invalid, the bracket takes the highest priority.
```

`typedef` can be used to simplify the naming of the structure.

```c
typedef struct date {
    enum day_name day;
    int day_num;
    enum month_name month;
    int year;
} Date;

Date big_day = {Mon, 7, Jan, 1980};
```

## Memory Alignment

Struct alignment is achieved by dividing struct memory space into equally sized segments.

The size of each segment is the size of the largest alignment. This may require padding bytes to be inserted between members to maintain proper data alignment

Address of a struct variable will give us direct access to bytes of the first members.
- Alignment depends on architecture
- Special compiler extensions can be used to prevent padding

```c
struct a {
    int x;
    short s1, s2;
    float y;
    char c1, c2, c3, c4;
};
sizeof (struct a) == 16

struct b {
    int x;
    short s1;
    float y;
    char c1;
};
sizeof (struct b) == 16

struct c {
    int x;
    short s1;
    char c1;
    float y;
};
sizeof (struct c) == 12
```
