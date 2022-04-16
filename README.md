# 0x11. C - printf
Foundations - Low-level programming & Algorithm ― Hatching out
by Julien Barbier, co-founder at Holberton School.
Project to be done in teams of 2 people (your team: Oliyad Kebede, Kaleb Ayelaw)

## Background Context
* Write your own `printf` function.

## Getting Started

* Allowed editors: vi, vim, emacs.
* All your files will be compiled on Ubuntu 14.04 LTS.
* Your programs and functions will be compiled with gcc 4.8.4 using the flags -Wall -Werror -Wextra and -pedantic.
* All your files should end with a new line.
* A README.md file, at the root of the folder of the project is mandatory.
* Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl.
* You are not allowed to use global variables.
* No more than 5 functions per file.
* In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples.
* The prototypes of all your functions should be included in your header file called holberton.h
* Don’t forget to push your header file.
* All your header files should be include guarded.
* Note that we will not provide the\_putchar function for this project


### Description

------------

printf is the C language function to do format-ted printing. The same function is also available in
PERL. The printf function sends formatted output to stdout.
A custom _printf() for learning purposes was developed by cohort  #9 students Jimmer and Edward Ortiz.
_printf() function format string is a character string, beginning and ending in its initial shift state, if any. 
These arguments are placed using the percentage '%' operator

------------


#### Resources

------------


Secrets of printfby Don colton
https://www.cypress.com/file/54761/download

------------



## Authorized functions and macros
* write (man 2 write)
* malloc (man 3 malloc)
* free (man 3 free)
* va_start (man 3 va_start)
* va_end (man 3 va_end)
* va_copy (man 3 va_copy)
* va_arg (man 3 va_arg)

#### Compilation

------------



The code must be compiled this way:

**$ gcc -Wall -Werror -Wextra -pedantic *.c**

As a consequence, be careful not to push any c file containing a main function in the root directory of your project (you could have a test folder containing all your tests files including main functions)

The main files will include your main header file (holberton.h): **#include holberton.h**

------------

#### Use & Examples


------------

**Prototype:** int _printf(const char *format, ...);
**Use - General:** _printf("format string", var1, var2, ...);

**Examples:**
 - Basic String: _printf("%s Holberton", "Hello");`
	 - Output: Hello Holberton

- Print integers: _printf("This is an array element: arr[%d]:%c", 32, arr[32]);`
	- Output: This is an array element arr[32]:A

Many other specifiers and flags were added and by combinig those the _printf() function generate a different ouput. The following list are the specifiers and flags allowed.

------------

#### Use & Examples


------------

###### Specifiers

Specifier                |Output                        |Examples |
|----------------|-------------------------------|-----------------------------|
| `c` | Character | y |
| `d` or `i` | Signed integer | 1024, -1024 |
| `s` | String of characters | Hello Holberton |
| `b` | Binary Representation of unsigned integer | 01010110 |
| `u` | Unsigned integer | 1024 |
| `o` | Unsigned octal | 432 |
| `x` | Unsigned hexadecimal integer | 3ca |
| `X` | Unsigned hexadecimal integer (uppercase) | 3CA |
| `S` | String with hex-ascii value replacing special chars | \x0A\x0A |
| `p` | Pointer address | 0x403212 |
| `r` | Reversed string of characters | dlroW olleH |
| `R` | ROT13 Translation of string | Uryyb |

###### Flags (In development...)

|Flag                |Description                        |
|----------------|-------------------------------|
| `-` |Left-justify the output within the field width that was given; Right justification is the default (see _width_ sub-specifier). |
| `+` |Preceeds the result with a plus or minus sign (`+` or `-`) even for positive numbers. By default, only negative numbers are preceded with a `-` sign. |
| `(space)` |If no sign is going to be written, a blank space is inserted before the value. |
| `#` |Used with `o`, `x` or `X` specifiers the value is preceeded with 0, 0x or 0X respectively for values different than zero. |
| `0` |Left-pads the number with zeroes (`0`) instead of spaces when padding is specified (see _width_ sub-specifier). |

###### Width (In development...)

|Width                |Description                        |
|----------------|-------------------------------|
| `(number)` |Minimum number of characters to be printed. If the value to be printed is shorter than this number, the result is padded with blank spaces. The value is not truncated even if the result is larger.|
| `*` | The _width_ is not specified in the _format_ string, but as an additional integer value argument preceding the argument that has to be formatted.|

### Precision (In development...)

|.Precision               |Description                        |
|----------------|-------------------------------|
| `.(number)` |**For integer specifiers (`d`, `i`, `o`, `u`, `x`, `X`):** _precision_ specifies the minimum number of digits to be written. If the value to be written is shorter than this number, the result is padded with leading zeros. The value is not truncated even if the result is longer. A _precision_ of 0 means that no character is written for the value 0. **For `s`**: this is the maximum number of characters to be printed. By default all characters are printed until the ending null character is encountered. If the period is specified without an explicit value for _precision_, 0 is assumed. |

### Lenght modifiers (In development...)

|Modifier/Specifier  |`d` & `i`  |`u`, `o`, `x`, `X` |`c` |`s` |`p` |
|----------------|---------|------------|-------------|-----|-------|
| `none` | int |unsigned int | int| char pointer| void pointer |
| `h` |short int|unsigned short int |     |     |              |
| `l` |long int |unsigned long int  |     |     |              |

------------

#### Files contained in this repository


------------

|Name                |Information                        |Relevant Files                         |
|----------------|-------------------------------|-----------------------------|
|`man_3_printf`|Man page of the _printf() function.| `None` |
|`holberton.h`	| Header file with the data type struct, standard libraries and custom prototypes.| `*.c compilation` |
|`_printf.c`|Main printf function file. Calls other functions.|`printf_(name of var).c file` |
|`printf_37.c`|Contains percentage print function.|`None` |
|`printf_int.c` | Contains decimal and integer functions. | `None` | 
`printf_char.c` | Custom function for char data type. | `None`
|`printf_sting.c` | Function that calls string type variable. | `None` |
|`printf_bin.c` | Function that gets the binary | `None` |
`printf_oct.c` | Functions that returns octal number. | `None` |
`printf_hex.c` | Calls hexadecimal numbers (lowercase). | `None` | 
`printf_HEX.c` | Calls hexadecimal numbers (Uppercase). | `None` |
`printf_unsigned.c` | Returns an unisgined data type. | `None` |
`printf_hex_aux.c` | Auxiliar function for hexadecimal specific functions (lowercase). | `printf_exclusive_string.c` | 
`printf_HEX_aux.c` | Auxiliar function hexadecimal specific functions (Uppercase). | `printf_p.c` |
`printf_exclusive_string.c` | Returns a string and non readable characters are printed in hexadecimal numbers (Lowercase). | `printf_hex_aux.c` |
`printf_srev.c` | Returns a string in reverse. | `None` |
`printf_rot13.c` | Returns a string in Rot13. | `None` |
`printf_str.c` | Auxiliar functions such as strlen and strcpy. | `None` |
`_putchar.c` | Custom putchar function. | `None` |


------------

#### Tasks required for this project

##### REPO: GitHub repository: printf
#
### 1. Education is when you read the fine print. Experience is what you get if you don't
#### Write a function that prints numbers, followed by a new line.
Handle the following conversion specifiers:
* d
* i
* You don’t have to handle the flag characters
* You don’t have to handle field width
* You don’t have to handle precision
* You don’t have to handle the length modifiers
##### REPO: GitHub repository: printf
#
### 2. Just because it's in print doesn't mean it's the gospel
#### Create a man page for your function.
##### REPO: GitHub repository: printf
##### File: man_3_printf
#
### 3. With a face like mine, I do better in print
#### Handle the following custom conversion specifiers:

* b: the unsigned int argument is converted to binary

##### REPO: GitHub repository: printf
#
### 4. What one has not experienced, one will never understand in print
#### Handle the following conversion specifiers:
* u
* o
* x
* X
* You don’t have to handle the flag characters
* You don’t have to handle field width
* You don’t have to handle precision
* You don’t have to handle the length modifiers

##### REPO: GitHub repository: printf
#
### 5. Nothing in fine print is ever good news
#### Use a local buffer of 1024 chars in order to call write as little as possible.

##### REPO: GitHub repository: printf
#
### 6. My weakness is wearing too much leopard print
#### Handle the following custom conversion specifier:
* S : prints the string.
* Non printable characters "(0 < ASCII value < 32 or >= 127)" are printed this way: \x, followed by the ASCII code value in hexadecimal (upper case - always 2 characters)
##### REPO: GitHub repository: printf
#
### 7. How is the world ruled and led to war? Diplomats lie to journalists and believe these lies when they see them in print
#### Handle the following conversion specifier: p.
* You don’t have to handle the flag characters
* You don’t have to handle field width
* You don’t have to handle precision
* You don’t have to handle the length modifiers

##### REPO: GitHub repository: printf
#
### 8. The big print gives and the small print takes away
#### Handle the following flag characters for non-custom conversion specifiers:
* \+
* space
* \#

##### REPO: GitHub repository: printf
#
### 9. Sarcasm is lost in print
#### Handle the following length modifiers for non-custom conversion specifiers:
* l
* h
Conversion specifiers to handle: d, i, u, o, x, X

##### REPO: GitHub repository: printf
#
### 10. Print some money and give it to us for the rain forests
#### Handle the field width for non-custom conversion specifiers.

##### REPO: GitHub repository: printf
#
### 11. The negative is the equivalent of the composer's score, and the print the performance
#### Handle the precision for non-custom conversion specifiers.

##### REPO: GitHub repository: printf
#
### 12. It's depressing when you're still around and your albums are out of print.
#### Handle the 0 flag character for non-custom conversion specifiers.

##### REPO: GitHub repository: printf
#
### 13. Every time that I wanted to give up, if I saw an interesting textile, print what ever, suddenly I would see a collection.
#### Handle the - flag character for non-custom conversion specifiers.

##### REPO: GitHub repository: printf
#
### 14. Print is the sharpest and the strongest weapon of our party.
#### Handle the following custom conversion specifier:
* r : prints the reversed string

##### REPO: GitHub repository: printf
#
### 15. The flood of print has turned reading into a process of gulping rather than savoring 
#### Handle the following custom conversion specifier:
* R: prints the rot13'ed string

##### REPO: GitHub repository: printf
#
### 16. *
#### All the above options work well together.
##### REPO:
* GitHub repository: printf
#

