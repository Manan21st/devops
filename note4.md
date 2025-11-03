# Introduction to Shell Scripting

## Shell Basics
Shell scripting is an essential skill for automating tasks in UNIX and Linux environments.  
A shell script is a simple program executed by the shell, which acts as a command line interpreter between the user and the operating system.

---

## Creating a Shell Script

1. Create a new file with a `.sh` extension, for example `hello_world.sh`.
2. Start the script with a shebang followed by the interpreter path, commonly: `#!/bin/bash`
3. Add shell commands and scripting logic to automate tasks.

---

## Script Execution

- Make the script executable using: `chmod +x filename.sh`
- Run the script using: `./filename.sh`

---

## Variables and Data Handling

- Variables are defined using: `VARIABLE_NAME=value`
By convention, uppercase letters are commonly used for variable names, for example: `USERNAME="JohnDoe"`

- Variables are accessed using the `$VARIABLE_NAME` syntax.

- User input can be read using: `read -p "Prompt: " VARIABLE`

---

## Conditionals and Loops

### Conditional Statements
- The `if` statement is used for conditional execution.
- Conditions are evaluated using square brackets: `if [ condition ]`
- Example file check:` -f filename`
This checks whether a file exists.

### Loops
- `for` and `while` loops are used to iterate over sequences or repeat tasks based on conditions.

---

## File Permissions and Management

### File and Directory Management
- Create directories using `mkdir`.
- Navigate directories using `cd`.
- Create files using `touch` or: `cat > filename`

### File Permissions
- Linux permissions are defined for users, groups, and others.
- Permissions include:
- `r` for read
- `w` for write
- `x` for execute
- Permissions can be modified using the `chmod` command.

### Advanced Permission Control
- Access Control Lists (ACLs) provide more fine grained permission control compared to traditional `chmod`.

---

## Common Shell Commands
Some essential shell commands include:
- `ls`  
- `pwd`  
- `cd`  
- `rm`  
- `cp`  
- `mv`  

Commands such as `rm -rf` should be used with caution as they remove files and directories recursively without confirmation.

---

## String Manipulation and Utilities

### String Manipulation
- Tools like `tr`, `sed`, and `awk` are used for text processing.
- Example for converting text to uppercase: `echo $STRING | tr [a-z] [A-Z]`

### Find and Locate Commands
- The `find` command is used to search for files based on name, type, or other attributes.
- Syntax: `find <path> -name <pattern>`

### Regular Expressions
- Regular expressions are useful for pattern matching and text processing in shell scripting.
- While not covered in depth, they are an important concept for advanced scripting.

---

## Advanced Scripting Concepts

### Function Definition and Usage
Functions allow reuse of code blocks. Ex: `my_function() { commands }`
Functions are called using their name: `my_function`

### User and Group Management
Shell scripts can automate system administration tasks such as:
- Creating users using `useradd`
- Creating groups using `groupadd`
- Assigning default shells, permissions, and welcome messages

---

## Conclusion
These notes cover key concepts of shell scripting, starting from basic script creation to advanced topics such as file permissions, user management, and text processing.  
Shell scripting is a powerful tool for automation and system administration in Linux environments.










