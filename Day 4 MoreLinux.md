# The Linux file hierarchy 
The Linux file hierarchy refers to the organization and structure of files and directories in a Linux system. It defines where different types of files and directories are located, making it easier for users and applications to find and access them. 

System files 
System files are files used by the system software(OS)
**Window**: system files appear 
**Linux**: System files appear under the root directory (/)under the local disk C:
Here's a brief overview of the main directories in the Linux file hierarchy:

1. **`/` (Root Directory)**:
    
    - The root directory is the top-level directory in the Linux file system hierarchy.
    - All other directories and files are located under the root directory.
    - It contains essential system files and directories necessary for the operation of the system.
2. **`/bin` (Binaries)**:
    
    - This directory contains essential executable binaries (programs) that are required for system booting and repair. Available in single-user mode. Example: cat, ls, cp, pwd
3. **`/boot` (Boot Loader Files)**:
    
    - Contains boot loader files, kernel images, and other files required for system booting.
    - It typically contains the following types of files:

A. **Bootloader Configuration Files**: Configuration files for bootloaders such as GRUB (GRand Unified Bootloader) are stored here. These files specify the location of the kernel and the initial RAM disk (initramfs) required for booting.
    
B. **Kernel Images**: The actual kernel image files (`vmlinuz`) are stored in this directory. The kernel is the core component of the operating system responsible for managing hardware resources and providing essential services.
    
C. **Initramfs (Initial RAM File System)**: The initramfs is an initial filesystem loaded into memory during the boot process before the actual root filesystem is mounted. It contains essential drivers and utilities needed to initialize hardware and prepare the system for booting.
    
D. **Bootloader Stage Files**: Some bootloaders store their stage files or other necessary components in the `/boot` directory. These files are responsible for loading the kernel and initiating the boot process.
    

By storing these critical files in a separate directory (`/boot`), it helps ensure that they are easily accessible and isolated from other parts of the filesystem. This separation also simplifies system maintenance and troubleshooting, as the boot-related files can be managed independently.

4. **`/dev` (Device Files)**:
    
    - Contains device files representing devices attached to the system, such as hard drives, USB drives, etc.
5. **`/etc` (Configuration Files)**:
    
    - Contains system-wide configuration files for various applications and services.
    - This also contains startup and shutdown shell scripts used to start/stop individual programs.
    
6. **`/home` (Home Directories)**:
    
    - Contains user home directories where users store their personal files and configurations. Example: /home/hermela , /home/rexder  
7. **`/lib` (Libraries)**:
    
    - Contains shared libraries needed by the essential binaries in `/bin` and `/sbin`.
8. **`/mnt` (Mount Point)**:
    
    - Typically used as a temporary mount point for mounting external storage devices like USB drives.
    - **The difference between /mnt and /dev**
    
     A. **/mnt (Mount Point)**:
    - The `/mnt` directory is used as a standard location for temporarily mounting external storage devices, network shares, or other filesystems.
    - When you want to access files on a USB drive, a network share, or any other external storage device, you typically mount it under the `/mnt` directory.
    - It is a convention for users to manually mount filesystems to `/mnt` when needed, although many Linux distributions may use other directories for this purpose as well.
     B.**/dev (Device Files)**:
    - The `/dev` directory contains special device files that represent devices attached to the system, such as hard drives, USB drives, CD-ROM drives, serial ports, and more.
    - These device files allow user programs and the operating system to communicate with and access hardware devices in a standardized way.
    - `/dev` is not intended for manual mounting of filesystems; instead, it provides access to device drivers and interfaces for system components.
    -
   9.**`/opt` (Optional Packages)**:
    - Contains optional software packages that are not part of the default installation.
10. **`/proc` (Process Information)**:
    
    - Contains virtual files that provide information about system processes and kernel parameters.
11. **`/root` (Root User Home Directory)**:
    
    - Home directory for the root user.
12. **`/sbin` (System Binaries)**:
    
    - Contains essential system administration binaries.
13. **`/tmp` (Temporary Files)**:
    
    - Used for storing temporary files that are only needed for a short period of time.
14. **`/usr` (User Programs and Data)**:
    
    - Contains user-accessible programs, libraries, documentation, and other data.
15. **`/var` (Variable Data)**:
    
    - Contains variable data files such as logs, spool files, and temporary files.

This is just a brief overview, and there are many more directories in the Linux file hierarchy, each serving specific purposes in the operation of the system.
**
What is the difference between the root directory(/) and root?
1. **/** (Root Directory):
    
    - The "/" represents the root directory of the file system hierarchy.
    - It is the starting point of the file system, from which all other directories and files are organized.
    - It is analogous to the root of a tree, from which all branches (directories) and leaves (files) stem.
    - All directories and files are located under the root directory ("/").
    - The root directory is denoted by a single forward slash ("/").
2. **root (Superuser)**:
# Text editors 
They are programs that used for text processing.
* Linux command line text editors are VIM, Nano, Emacs, Neovim 
* Linux Graphical Text editors(downloaded software) like: Sublime, Vscode, :Pluma,  Gedit
###  VIM
* Here's a brief overview of how to get started with Vim and its syntax:

1. **Opening a File**:
    
    - To open a file with Vim, you can type `vim` followed by the filename in the terminal.
    - For example:
        `vim filename.txt`
        
2. **Modes**:
    - Vim has different modes for different purposes:
        - **Normal Mode**: This is the default mode for navigation and issuing commands.
        - **Insert Mode**: In this mode, you can insert and edit text.
        - **Visual Mode**: This mode allows you to select and manipulate text visually.
        - **Command-Line Mode**: This mode is used for entering commands such as saving and quitting.
3. **Basic Navigation**:
    
    - Use the arrow keys or `h`, `j`, `k`, `l` to move the cursor left, down, up, and right respectively.
    - You can also use various navigation commands such as `gg` to move to the beginning of the file, `G` to move to the end of the file, and `:n` to move to a specific line number.
4. **Editing Text**:
    
    - Press `i` to enter Insert Mode and start typing.
    - Press `Esc` to exit Insert Mode and return to Normal Mode.
    - Use `dd` to delete a line, `yy` to yank (copy) a line, and `p` to paste it.
5. **Saving and Quitting**:
    
    - To save changes and quit Vim, you can use the `:wq` command.
    - To quit without saving changes, you can use the `:q!` command.
    - To quit and save changes by forcing it, you can use the :wq! command.
    - To undo, you can use **:undo or :u** command
    - To execute commands :%!your command   **(Note: the is no space between the symbols and your command)**
1. **Syntax Highlighting**

    - Vim supports syntax highlighting for various programming languages and file types.
    - To enable syntax highlighting, you can use the `:syntax on` command while in Normal Mode.
7. **Customization**:
    
    - Vim is highly customizable, and you can customize its behavior by editing the `.vimrc` file in your home directory.
    - You can also install plugins to extend Vim's functionality.
  **Nano**
Nano is a straightforward and user-friendly text editor commonly found on Unix-based systems, including Linux. 
Basic guide on how to use Nano and its syntax:

1. **Opening a File**:
    
    - To open a file with Nano, simply type `nano` followed by the filename in the terminal.
    - For example:
        `nano filename.txt`
        
2. **Basic Navigation**:
    
    - Use the arrow keys to move the cursor.
    - You can also use the `Page Up` and `Page Down` keys to navigate larger distances.
3. **Editing Text**:
    
    - Nano has simple keyboard shortcuts for basic text editing:
        - `Ctrl + O`: Save the file (Write Out).
        - `Ctrl + X`: Exit Nano.
        - `Ctrl + G`: Get Help (display Nano's help menu).
        - `Ctrl + K`: Cut the current line.
        - `Ctrl + U`: Uncut (paste) the cut text.
        - `Ctrl + W`: Search for text within the file.
    - To start typing, simply place the cursor where you want to insert text and start typing.
4. **Syntax Highlighting**:
    
    - By default, Nano doesn't have syntax highlighting like some other text editors. However, you can enable it by using the `-Y` flag when opening a file.
    - For example:
        
        Copy code
        
        `nano -Y php filename.php`
        
5. **Indentation**:
    
    - Nano doesn't have automatic indentation features like some other editors. You'll need to manually indent your code by pressing the `Tab` key.
6. **Saving and Quitting**:
    
    - To save changes and exit Nano, press `Ctrl + O`, then press `Enter`, and finally press `Ctrl + X` to exit.
    - If you don't want to save changes, press `Ctrl + X`, and Nano will ask if you want to save changes before exiting.
7. **Other Features**:
    
    - Nano has a menu at the bottom with helpful information and options.
    - You can access the menu by pressing `Ctrl + G` for help.
# Linux User Management 
+ Every users have Group and have their own file and application
+ On computer system, person who uses the computer is called **User**.1.
1. Creating a user
    - You can create a new user account using the `useradd` command followed by the username
        `sudo useradd username`
        
    - Optionally, you can specify additional options such as the user's home directory and default shell.
    OR
    
     To create a new user account, you can use the `adduser` command followed by the desired username:
    
        `sudo adduser username`
        
    - This command will prompt you to enter additional information for the new user, such as the user's full name, room number, work phone, and home phone. You can skip these details by pressing `Enter` for each prompt.
2. **Setting a Password**:
    
    - After creating a user, you'll need to set a password for the user account using the `passwd` command:
        
        Copy code
        
        `sudo passwd username`
        
    - You'll be prompted to enter and confirm the new password.
3. **Modifying User Properties**:
    
    - You can modify user properties such as the user's home directory, default shell, and account expiration date using the `usermod` command.
    - For example, to change the default shell for a user:
        
        bashCopy code
        
        `sudo usermod -s /bin/bash username`
        
4. **Deleting a User**:
    
    - To delete a user account, use the `userdel` command followed by the username:
        
        Copy code
        
        `sudo userdel username`
        
    - By default, this command only removes the user account and its home directory, but not the user's files. To remove the user's files as well, use the `-r` option:
        
        Copy code
        
        `sudo userdel -r username`
        
5. **Managing Groups**:
    
    - Users in Linux belong to one or more groups, which define their access permissions to files and resources.
    - You can create a new group using the `groupadd` command:
        
        Copy code
        
        `sudo groupadd groupname`
        
    - Add a user to a group using the `usermod` command with the `-aG` option:
        
        Copy code
        
        `sudo usermod -aG groupname username`
        
6. **Granting Sudo Privileges**:
    
    - Sudo (short for "superuser do") allows users to run commands with the privileges of another user, typically the root user.
    - To grant sudo privileges to a user, add the user to the `sudo` or `wheel` group, depending on your Linux distribution:
        
        graphqlCopy code
        
        `sudo usermod -aG sudo username   # For Ubuntu and Debian sudo usermod -aG wheel username  # For CentOS and Fedora`
        
7. **Viewing User Information**:
    
    - You can view information about users and groups using commands like `id`, `finger`, `getent`, or by inspecting files like `/etc/passwd` and `/etc/group`.
**NOTE: The user files are stored inside /etc/passwd
      : The user password are stored inside /etc/shadow
### To access root user
Command 
+ sudo su