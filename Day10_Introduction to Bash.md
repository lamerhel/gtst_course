# What is Bash?
Bash, short for Bourne-Again Shell, is a Unix shell and command language supported by the Free Software Foundation and first developed by Brian Fox for the GNU Project[1](https://www.javatpoint.com/bash-introduction)[2](https://phoenixnap.com/kb/what-is-bash). It is designed as a free software alternative for the Bourne shell, initially released in 1989[5](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29). Bash is a shell program that provides an environment for users to issue commands and run other applications[2](https://phoenixnap.com/kb/what-is-bash). It is a versatile and customizable shell, packed with features that allow casual users, programmers, and system administrators to use the command line effectively[2](https://phoenixnap.com/kb/what-is-bash).Bash is a command-line interpreter that typically runs in a text window where users can interpret commands to carry out various actions[1](https://www.javatpoint.com/bash-introduction). The combination of these commands as a series within a file is known as a Shell Script. Bash can read and execute the commands from a Shell Script[1](https://www.javatpoint.com/bash-introduction). Bash is the default login shell for most Linux distributions and Apple's macOS[1](https://www.javatpoint.com/bash-introduction). It is also accessible for Windows 10 with a version and default user shell in Solaris 11[1](https://www.javatpoint.com/bash-introduction).

Bash is a shell that used to interact with your kernel.
+ script is a file that contains shell commands in a simple and clear algorithm 
### use of bash

- Script development
- Automating tasks
-  Simplifying your Linux ability
- Developing hacking scripts.
Bash (Bourne Again Shell) is indeed both a shell and a programming language. As a shell, it provides an interface for users to interact with the operating system, executing commands and managing files. As a programming language, Bash allows users to write scripts to automate tasks, control program flow, and perform various operations such as string manipulation, file handling, and arithmetic calculations.

Other shells like sh (Bourne Shell), zsh (Z Shell), and fish (Friendly Interactive Shell) also serve as both shells and programming languages, although they have different features and syntaxes.

- **sh (Bourne Shell)**: The original Unix shell, sh, is a simple shell that provides basic functionality for interacting with the operating system. It is often used for scripting but lacks some of the more advanced features found in modern shells like Bash.
    
- **zsh (Z Shell)**: Zsh is an extended version of sh with additional features for interactive use and scripting. It offers advanced capabilities such as improved tab completion, powerful globbing, and more advanced scripting capabilities compared to sh.
    
- **fish (Friendly Interactive Shell)**: Fish is designed to be user-friendly with features like syntax highlighting, autosuggestions, and easy-to-understand syntax. While fish is not POSIX-compliant like sh and zsh, it offers a more modern and intuitive experience for interactive shell usage.
## Starting with Bash

- Bash files can have “.sh” extension but you can have it without ‘.sh’ too
- The file have to have executable Permission
- You can use any text editors u need: VIM,nano,VScode,gedit,cherrytree…
### Displaying the output

- To start Every bash scripts use shebang.
- #! /bin/bash
- #! /bin/sh
- To display outputs on bash you just do ***echo “YOUR TEXT HERE”***
 **To run your project you can do(Don't forget to the file):**
- /bin/bash hello.sh
- ./hello.sh   ->  need x
- hello -> need x (you can make execute using **chmod +x hello.sh**command )
**Note: by default when the bash file is created, it has no permission for execution**
## The use of Shebang
The shebang (#!) is a special character sequence at the beginning of a script, followed by the path to the interpreter. Its main purpose is to tell the system which interpreter should be used to execute the script. Here's a breakdown of its usage:

1. **Interpreter Specification**: The shebang line is usually the first line in a script file. It starts with #! followed by the path to the interpreter that should execute the script. For example:
    `#!/bin/bash`
    In this case, the shebang specifies that the Bash interpreter located at `/bin/bash` should be used to execute the script.
    
2. **Cross-Platform Compatibility**: Shebangs are particularly useful in environments where different scripting languages or interpreters may be available. They ensure that the script runs with the intended interpreter regardless of the user's configuration.
    
3. **Executable Scripts**: Shebangs are essential for making scripts directly executable. After setting the shebang line and making the script file executable with appropriate permissions (e.g., `chmod +x script.sh`), users can run the script without explicitly specifying the interpreter.
4. **Script Portability**: Shebangs enable script portability across different systems and platforms. For instance, a script with `#!/bin/bash` as the shebang line will run on systems where Bash is installed, regardless of its location.
    
5. **Custom Interpreters**: Shebangs can specify custom interpreters or environments. For example, you might use `#!/usr/bin/python3` for Python 3 scripts or `#!/usr/bin/env node` for Node.js scripts, allowing users to run scripts with the appropriate interpreter without knowing its absolute path.
### variables
**- Bash Variables are same with python variables, with some exceptions.
- Syntax:
- VARIABLE_NAME=value 
**Exceptions:**
- NO Space between the equal sign ( = )
- NAME  =  “Nathan”   => ERROR
- NAME=”Nathan”  =>  Correct.
- Never Start with Numbers
- USE double quotes only.
- To use the variable we will use dollar sign( $ )  before the Variable name.
- If you want to display the variable sticked with other text use ${VARIABLE_NAME}
- Bash Variables are string by default.**

- The set command can be used to assign values to positional parameters.
- Syntax:
`set value1 value2 value3 value4 value5`
## system variables
`echo $USER` used to display the computer owner or the host.
We can not use the systems variables as a variable that we create
### variables and data types
As we saw, the previous method they create strings only.
- So to create other data types we use declare.
- Arrays
1. Arrays are lists or tuples on python.
2. Syntax:  `var=(“list1” “list2” “list3” “list4)`
+ TO display `echo ${var[0]}`
+ To get all the elements: `echo ${var[@]}`
+ To get the indexes `echo ${!var[@]}`
+  To get the length  `echo ${#var[@]}`
+ To add element to the array `var[4]=”list5”`
+ To remove from the array `unset var[3]`






