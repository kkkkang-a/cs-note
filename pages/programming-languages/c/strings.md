# Strings

Strings may be initialised at the time of declaration using an “array-like” notational convenience

```c
char greetings[] = "Hello World!";
```

Unlike many other programming languages, C does not have a String type to easily create string variables. Instead, strings resemble an [array](./arrays.md) of characters

However, in C, all strings are NULL-terminated. NULL is the binary value 0 (denoted ‘\0’), not the ASCII representation of the character 0.

```c
char myHobby[] = "rowing";  // ’r’’o’’w’’i’’n’’g’’\0’
```

