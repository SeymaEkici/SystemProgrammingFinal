Command Line Utility
====================

Overview
--------

This is a simple command-line utility written in C that accepts user input, tokenizes commands, and executes them accordingly. It provides basic shell-like functionality such as changing directories, listing files, displaying file contents, and executing system commands.

Features
--------

-   **cd** - Changes the current working directory.
-   **ls** - Lists files in the current directory (uses `dir` for Windows compatibility).
-   **pwd** - Prints the current working directory.
-   **echo** - Prints the specified text to the console.
-   **cat** - Displays the contents of a file.
-   **rm** - Deletes the specified file.
-   **history** - Placeholder for command history functionality.
-   **help** - Displays available commands.
-   Executes other commands using `CreateProcess`.

Requirements
------------

-   Windows OS
-   C compiler (MinGW, MSVC, etc.)

Compilation
-----------

To compile the program using GCC:

```
gcc main.c -o command_utility

```

Usage
-----

Run the compiled executable and enter commands interactively:

```
./command_utility

```

Then, enter commands such as:

```
cd C:\Users
ls
echo Hello, World!
cat example.txt
rm test.txt

```

Notes
-----

-   The program uses `_chdir()` and `_getcwd()` for directory operations (Windows-specific functions).
-   `CreateProcess()` is used to execute unknown commands.
-   Error handling is implemented for invalid commands and missing arguments.

Future Improvements
-------------------

-   Implement command history.
-   Improve error handling.
-   Add support for additional shell commands.

License
-------

This project is open-source and available for modification.
