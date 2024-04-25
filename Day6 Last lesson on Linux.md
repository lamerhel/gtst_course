# Script Installation
Script installation on Linux typically refers to the process of installing software using a script. This script could be a shell script (usually with a `.sh` extension) or another type of script designed to automate the installation process.

Here's a general overview of how script installation works:

1. **Downloading the script**: You'll need to obtain the installation script from a trusted source. This could be from the software's official website, a version control repository like GitHub, or a package manager's repository.
    
2. **Inspecting the script (optional)**: Before running any script, especially if obtained from an untrusted source, it's a good idea to inspect its contents to ensure it's safe to run. You can review the script using a text editor or a command-line tool like `less` or `cat`.
    
3. **Making the script executable**: If the script is not already executable, you'll need to make it so using the `chmod` command. For example:
    `chmod +x install-script.sh`
    
4. **Running the script**: Execute the script by running it with appropriate permissions. This is typically done by invoking it with `./` followed by the script name. For example:
    `./install-script.sh`
    
5. **Following prompts (if any)**: Depending on the script, you may be prompted to provide input or confirm certain actions during the installation process. Follow the prompts as necessary. 
    
6. **Completion**: Once the script has finished running, the software should be installed on your system. You may need to perform additional steps such as configuring the software or adding it to your system's PATH.
To install script from GitHub We can use: ***git clone {link of the script for GitHub}***

Note: **Downloading a script typically involves obtaining the installation script itself, not the software it installs. The script is essentially a set of instructions that automates the process of installing the software on your system.

**When you download the script, you're obtaining a file that contains the necessary commands and actions to install the software. You then run this script to execute those commands and install the software on your system.

**So, downloading the script is the first step in the process. After that, you'll run the script to actually install the software on your system. Once the script finishes running, the software should be installed and ready to use on your system.**

Script installation can be convenient for installing software that isn't available through your distribution's package manager or for automating complex installation procedures. However, it's essential to ensure that you're running scripts from trusted sources to avoid potential security risks.

## Script Module

- Scripts are made with scripting languages(programming) like { python,bash,go,ruby,...}
- So when we use these programming languages to do tasks their is something called modules/libraries these are needed to run the script as the dependencies.
Example:
Python: to install python modules we use -> pip install {moudulename}
    For requirements file -> pip install -r requirements.txt
 Go: to install go modules -> go install {modulename}
3. Ruby:  to install ruby modules -> gem install {modulename}

### Foreground and background 
In Linux, "foreground" and "background" have similar meanings to their general computing context but are often associated with processes and job control within the operating system:

1. **Foreground**:
    
    - In Linux, the foreground refers to the currently active process or command that is running in a terminal and is receiving input from the user.
    - When you execute a command in a terminal without sending it to the background, it typically runs in the foreground. The command holds control of the terminal until it completes or is suspended.
    - While a process is running in the foreground, it may produce output that is displayed directly in the terminal.
2. **Background**:
    
    - In Linux, background processes are those that are running independently of the foreground process and do not receive input from the user directly.
    - When you run a command in the background, it continues to execute concurrently with other commands, and you regain control of the terminal to enter additional commands.
    - You can start a command in the background by appending an ampersand `&` to the command when you execute it in the terminal. For example:
        `long-running-command&`
        
    - Background processes often perform tasks that do not require immediate user interaction or that can run concurrently with other tasks.
    - To get the background process back to foreground type ***fg*** and then enter.
    - To stop a process going inside your shell just press ***ctrl + c*** and ***ctrl + z*** to run in the background. 
    **Null Device**
    In Linux, the "null device" refers to a special device file named `/dev/null`. This device file discards all data written to it and provides no data when read from. It essentially acts as a data sink, absorbing any data written to it without storing it anywhere or providing any output.

Here's what you need to know about the null device:

1. **Discarding Output**: When data is written to `/dev/null`, it is simply discarded by the operating system. This is useful when you want to suppress the output of a command or program, redirecting it to nowhere.
    
2. **Silencing Output**: Administrators and developers often use `/dev/null` to silence unwanted output. For example, if you want to run a command but don't want to see its output in the terminal, you can redirect the output to `/dev/null`.
    
3. **Example Usage**:
    
    - To discard the output of a command:
        
        `command > /dev/null`
        
    - To discard both standard output and standard error:
        
        `command > /dev/null 2>&1`
        
    - To discard the output of a command and only see errors:
        
        `command 2> /dev/null`
        
4. **Reading from `/dev/null`**: Reading from `/dev/null` always returns an end-of-file (EOF) immediately, as there is no data stored in the null device.
    
5. **Permission**: `/dev/null` is typically accessible to all users and has permissions set to allow both reading from and writing to it.

    

In summary, the null device `/dev/null` is a special device file in Linux that discards all data written to it and provides no data when read from. It is commonly used to silence output or to discard unwanted data.