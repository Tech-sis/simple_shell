# Simple shell project

A simple UNIX command interpreter written as part of the low-level programming and algorithm track at ALX-Holberton School.


## Description

Custom version UNIX command language interpreter that reads commands from either interactive mode and non-interactive mode.

## Requirements

Allowed editors: vi, vim, emacs

Programs and functions will be compiled with gcc 4.8.4 using the flags -Wall -Werror -Wextra and -pedantic

All files should end with a new line
Code should use the Betty style. it will be checked using [betty-style.pl](https://github.com/holbertonschool/Betty/blob/master/betty-style\ .pl) and betty-doc.pl

No more than 5 functions per file
All your header files should be include guarded

Use system calls only when you need to
Authorized functions and system calls:
+ access (man 2 access)
+ chdir (man 2 chdir)
+ close (man 2 close)
+ closedir (man 3 closedir)
+ execve (man 2 execve)
+ exit (man 3 exit)
+ fork (man 2 fork)
+ free (man 3 free)
+ stat (__xstat)(man 2 stat)
+ lstat (__lxstat)(man 2 lstat)
+ fstat (__fxstat)(man 2 fstat```)
+ getcwd (man 3 getcwd)
+ getline (man 3 getline)
+ kill (man 2 kill)
+ malloc (man 3 malloc)
+ open (man 2 open)
+ opendir (man 3 opendir)
+ perror (man 3 perror)
+ read (man 2 read)
+ readdir (man 3 readdir)
+ signal (man 2 signal)
+ strtok (man 3 strtok)
+ wait (man 2 wait)
+ waitpid (man 2 waitpid)
+ wait3 (man 2 wait3)
+ wait4 (man 2 wait4)
+ write (man 2 write)
+ _exit (man 2 _exit)
+ isatty (man 3 isatty)
+ fflush (man 3 fflush)

## Usage

All the files are to be compiled on an Ubuntu 20.04 LTS machine with:

	gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh

Once compiled, to start the program, run: ./hsh

To exit the program, run: $ exit

This simple shell supports most shell commands, such as cat, pwd, ls -la and more.

## List of Functions

| Function Name      | Description |
| ----------- | ----------- |
|_strstr	|Locates a substring.|
|_strlen	|Returns a string.|
|_strcpy	|Copies a string pointed to by src to dest.|
|_strcat	|Concatenates two strings.|
|_strcmp	|Compare two strings.|
|_strdup	|Copies a string to another.|
|shellby_alias |Builtin command that eithe prints all aliases, specific aliases, or sets an alias.|
|set_alias |Will either set an existing alias 'name' with a new valu,'value' or creates a new alias with 'name' and 'value'.|
|print_alias |Prints the alias in the format name='value'.|
|replace_aliases |Goes through thearguments and replace any matching alias with their value.|
|get_builtin | Matches a command with a corresponding shellby builtin function.|
|shellby_exit  |Causes normal process termination for the shellby shell.|
|shellby_cd  |Changes the current directory of the shellby process.|
|shellby_help  |Displays information about shellby builtin commands.|
|help_all  |Displays all possible builtin shellby commands.|
|help_alias | Displays information on the shellby builtin command 'alias'.|
|help_cd | Displays information on the shellby builtin command 'cd'.|
|help_exit  |Displays information on the shellby builtin command 'exit'.|
|help_help  |Displays information on the shellby builtin command 'help'.|
|help_env | Displays information on the shellby builtin command 'env'.|
|help_setenv  |Displays information on the shellby builtin command 'setenv'.|
|help_unsetenv | Displays information on the shellby builtin command 'unsetenv'.|
|shellby_env  |Prints the current environment.|
|shellby_setenv | Changes or adds an environmental variable to the PATH.|
|shellby_unsetenv  |Deletes an environmental variable from the PATH.|
|_copyenv  |Creates a copy of the environment.|
|free_env  |Frees the the environment copy.|
|_getenv | Gets an environmental variable from the PATH.|
|error_env  |Creates an error message for shellby_env errors.|
error_1 |Creates an error message for shellby_alias errors.|
|error_2_exit  |Creates an error message for shellby_exit errors.|
|error_2_cd  |Creates an error message for shellby_cd errors.|
|error_2_syntax | Creates an error message for syntax errors.|
|error_126 | Creates an error message for permission denied failures.|
|error_127  |Creates an error message for command not found failures.|
|num_len | Counts the digit length of a number.|
| _itoa | Converts an integer to a string.|
 |create_error  |Writes a custom error message to stderr.|
|_realloc  |Reallocates a memory block using malloc and free.|
|assign_lineptr | Reassigns the lineptr variable for _getline.|
_getline | Reads input from a stream.|
|free_args | Frees up memory taken by args.|
|get_pid | Gets the current process ID.|
|get_env_value | Gets the value corresponding to an environmental variable.|
|variable_replacement | Handles variable replacement.|
|handle_line  |Partitions a line read from standard input as needed.|
|get_new_len  |Gets the new length of a line partitioned by ";", "||", "&&&", or "#".|
|logical_ops  |Checks a line for logical operators "||" or "&&".|
|get_args  |Gets a command from standard input.|
|call_args | Partitions operators from commands and calls them.|
|run_args | Calls the execution of a command.|
|handle_args | Gets, calls, and runs the execution of a command.|
|check_args | Checks if there are any leading ';', ';;', '&&', or '||'.|
|add_alias_end  |Adds a node to the end of a alias_t linked list.|
|add_node_end  |Adds a node to the end of a list_t linked list.|
|free_alias_list | Frees a alias_t linked list.|
|free_list | Frees a list_t linked list.|
|get_location | Locates a command in the PATH.|
|fill_path_dir | Copies path but also replaces leading/sandwiched/trailing colons (:) with current working directory.|
|get_path_dir | Tokenizes a colon-separated list of directories into a list_s linked list.|
|sig_handler | Prints a new prompt upon a signal.|
|execute | Executes a command in a child process.|
|main  |Runs a simple UNIX command interpreter.|
|cant_open  |If the file doesn't exist or lacks proper permissions, print a cant open error.|
|proc_file_commands  |Takes a file and attempts to run the commands stored within.
|token_len | Locates the delimiter index marking the end of the first token contained within a string.|
|count_tokens |Counts the number of delimited words contained within a string.|
|_strtok  |Tokenizes a string.|

## Builtin Commands

The following built-ins are supported by the Mr. Robot:

+ env - Print the current environment
+ exit - exit program sucessfully
+ cd - changes the current directory of the process to DIRECTORY.
+ alias -  prints a list of all aliases, one per line, in the form NAME
+ setenv - initializes a new environment variable, or modifies an existing one.
+ unsetenv - removes an environmental variable.

## Authors

#### Adeola Abilawon 
#### David Oloyede

## Acknowledgements
Shellby emulates basic functionality of the sh shell. This README borrows form the Linux man pages sh(1) and dash(1).

This project was written as part of the curriculum for ALX Holberton School. ALX Holberton School is a campus-based full-stack software engineering program that prepares students for careers in the tech industry using project-based peer learning.











