# Files

Disk storage peripherals provide persistent storage with a low-level interface. Operating systems arrange this into an abstraction known as files.

Read or write operations on a file are performed through System Calls.

A stream is associated with a file. It may have the following characteristics:
- **File Position Indicator**: This indicates the current position within the file and typically ranges from 0 to the file's length.
- **Binary or Text Mode**: A file stream can be opened in binary mode for handling raw binary data or in text mode for handling text data, which may involve character encoding conversions (e.g., ASCII, multibyte).
- **Open/Closed/Flushed State**: A file stream can be in one of several states, including open, closed, or flushed. An open stream allows reading from or writing to the associated file, a closed stream cannot perform I/O operations, and a flushed stream ensures that any buffered data is written to the file.
- **Buffering**: File streams can have different buffering modes:
    - *Unbuffered*: Each I/O operation directly affects the file without buffering.
    - *Fully Buffered*: Data is read or written in large chunks, improving performance by reducing the number of system calls.
    - *Line Buffered*: Data is buffered until a newline character is encountered, suitable for handling text files line by line.

System calls and stream operations provide the necessary functionality for interacting with files in a programmatic manner.

