0x11. C - printf

Requirements
General

    Allowed editors: vi, vim, emacs
    All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
    All your files should end with a new line
    A README.md file, at the root of the folder of the project is mandatory
    Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
    You are not allowed to use global variables
    No more than 5 functions per file
    In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
    The prototypes of all your functions should be included in your header file called main.h
    Don’t forget to push your header file
    All your header files should be include guarded
    Note that we will not provide the _putchar function for this project

GitHub

There should be one project repository per group. The other members do not fork or clone the project to ensure only one of the team has the repository in their github account otherwise you risk scoring 0%
More Info
Authorized functions and macros

    write (man 2 write)
    malloc (man 3 malloc)
    free (man 3 free)
    va_start (man 3 va_start)
    va_end (man 3 va_end)
    va_copy (man 3 va_copy)
    va_arg (man 3 va_arg)

Compilation

    Your code will be compiled this way:

$ gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c

    As a consequence, be careful not to push any c file containing a main function in the root directory of your project (you could have a test folder containing all your tests files including main functions)
    Our main files will include your main header file (main.h): #include main.h
    You might want to look at the gcc flag -Wno-format when testing with your _printf and the standard printf. Example of test file that you could use:

Compilation

    Your code will be compiled this way:

$ gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c


Understanding printf:

The printf function in C is used to display output to the console or file, using a formatted string as the first argument. The formatted string can contain conversion specifiers, which begin with a percent sign ("%") and are followed by a character that determines the type of the argument to be displayed.

Here's a list of the conversion specifiers in printf:

- %d or %i: Display an integer in decimal format. The difference between %d and %i is only in the interpretation of the argument.

- %o: Display an integer in octal (base 8) format.

- %x or %X: Display an integer in hexadecimal (base 16) format, with lowercase or uppercase letters, respectively.

- %u: Display an unsigned integer in decimal format.

- %c: Display a character.

- %s: Display a null-terminated string.

- %f: Display a floating-point number in decimal format.

- %e or %E: Display a floating-point number in scientific notation, with lowercase or uppercase letters, respectively.

- %g or %G: Display a floating-point number in either decimal or scientific notation, depending on its magnitude.

- %p: Display a pointer address in hexadecimal format.

Let's take a closer look at each conversion specifier.

%d or %i:
These two specifiers are used to display signed integers in decimal format. The difference between %d and %i is that %i interprets the argument as an integer in either decimal, octal, or hexadecimal format, depending on its prefix (if any). Both specifiers expect an int argument.

%o:
This specifier is used to display unsigned integers in octal (base 8) format. It expects an unsigned int argument.

%x or %X:
These specifiers are used to display unsigned integers in hexadecimal (base 16) format, with lowercase or uppercase letters, respectively. They expect an unsigned int argument.

%u:
This specifier is used to display unsigned integers in decimal format. It expects an unsigned int argument.

%c:
This specifier is used to display a single character. It expects an int argument, which is interpreted as an ASCII code.

%s:
This specifier is used to display a null-terminated string. It expects a char* argument, which points to the first character of the string.

%f:
This specifier is used to display floating-point numbers in decimal format. It expects a double argument.

%e or %E:
These specifiers are used to display floating-point numbers in scientific notation, with lowercase or uppercase letters, respectively. They expect a double argument.

%g or %G:
These specifiers are used to display floating-point numbers in either decimal or scientific notation, depending on their magnitude. They expect a double argument.

%p:
This specifier is used to display pointer addresses in hexadecimal format. It expects a void* argument, which points to the address to be displayed.

In addition to the conversion specifiers, the formatted string can also contain other characters, such as spaces, tabs, newlines, and literal percent signs ("%"). To include a literal percent sign in the output, you need to use "%%".

In conclusion, the printf function in C is a powerful tool for displaying formatted output to the console or file. Its conversion specifiers allow you to display a wide range of data types and formats, and its flexibility makes it a popular choice for debugging and general-purpose output.
