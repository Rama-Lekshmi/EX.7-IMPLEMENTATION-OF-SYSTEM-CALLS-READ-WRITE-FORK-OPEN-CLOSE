# EX.7-IMPLEMENTATION-OF-SYSTEM-CALLS-READ-WRITE-FORK-OPEN-CLOSE

# AIM:
C program using open, read, write, close , create , fork() system calls.

# ALGORITHM:
There are 5 basic system calls that Unix provides for file I/O.

1.create: Used to Create a new empty file

Syntax : int create(char *filename, mode_t mode)

filename : Name of the file which you want to create

mode : Indicates permissions of new file.

open: Used to Open the file for reading, writing or both. Syntax: int open(char *path, int flags [ , int mode ] );

Path : Path to file which you want to use

Flags : How you like to use ?

O_RDONLY: read only, O_WRONLY: write only, O_RDWR: read and write, O_CREAT: create file if it doesn’t exist, O_EXCL: prevent creation if it already exists

close: Tells the operating system you are done with a file descriptor and Close the file which pointed by fd. Syntax: int close(int fd); fd :file descriptor

read: From the file indicated by the file descriptor fd, the read() function reads cnt bytes of input into the memory area indicated by buf. A successful read() updates the access time for the file. Syntax: int read(int fd, char *buf, int size);

fd: file descripter buf: buffer to read data from cnt: length of buffer

write: Writes cnt bytes from buf to the file or socket associated with fd. cnt should not be greater than INT_MAX (defined in the limits.h header file). If cnt is zero, write() simply returns 0 without attempting any other action. Syntax: int write(int fd, char *buf, int size);

fd: file descripter buf: buffer to write data to cnt: length of buffer

*File descriptor is integer that uniquely identifies an open file of the process.

# PROGRAM:
```
Start the program.

Open a file for O_RDWR for R/W,O_CREATE for creating a file ,O_TRUNC for truncate a file.

Using getchar(), read the character and stored in the string[] array.

The string [] array is write into a file close it.

Then the first is opened for read only mode and read the characters and displayed it and close the file.

Use Fork().

Stop the program.
```

# OUTPUT:
![os 7 1](https://github.com/Rama-Lekshmi/EX.7-IMPLEMENTATION-OF-SYSTEM-CALLS-READ-WRITE-FORK-OPEN-CLOSE/assets/118541549/24b276fa-9d98-467c-9209-6ac04ebb9ccf)

# RESULT:
Thus, open, read, write, close , create , fork() system calls implemented successfully using c program.
