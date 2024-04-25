## Some advanced user commands
To change password of user
+ sudo passwd username
To change user id
+ sudo usermod -u new_id username
To delete user 
+ sudo userdel -r username
The `hostname` command in Linux is used to display or set the system's hostname. The hostname is the name assigned to a computer or a system on a network. When you run the `hostname` command without any arguments, it simply displays the current hostname of the system.
**To return to your /home use *cd ..***
## Sudoers file
+ The sudoers file is a file Linux and Unix administrators use to allocate system rights to system users.
- The user you created doesn’t have power to use sudo as the original one. 
- This is Because it is not Added in the sudoers file ( የSudoዎች file )
- To access this file
    **sudo visudo**
Note: In the Nano text editor in Linux, the `#` symbol is used to denote comments in configuration files or scripts. When you're editing a file that uses a syntax where `#` indicates comments, anything on a line following a `#` symbol will be considered a comment and will be ignored by the interpreter or application reading that file.

To change the username of an existing user in Linux, you typically use the `usermod` command. Here's how you can do it:

1. **Login as root or use sudo**: You need superuser privileges to change a user's information.
    
2. **Open a terminal**: Use your preferred terminal emulator.
    
3. **Use the usermod command**: The syntax for changing the username is as follows:
    `sudo usermod -l new_username old_username`
    
    Replace `new_username` with the desired new username and `old_username` with the current username you want to change.
    
    For example, if you want to change the username from `olduser` to `newuser`, you would run:
    `sudo usermod -l newuser olduser`
    
4. **Rename the user's home directory (Optional)**: By default, the user's home directory will remain the same as the old username. If you want to change the home directory name to match the new username, you can use the `-m` option with `usermod`:
    `sudo usermod -l new_username -m old_username`
    
    This will rename the home directory to match the new username.
    
5. **Verify the changes**: After running the command, you can verify that the username has been changed by listing the `/home` directory or by using the `id` command with the new username:
    `id new_username`
    This will display information about the user, including the username.
    Or you can use sudo mv old_username new_username

**To change the shell of a user use: *sudo usermod {username} -s /bin/bash***
To rename the file in your user(in your case kali) use: ***mv old_name new_name***

## Linux File Permission
File permissions in Linux determine who can read, write, and execute a file. They are represented by a set of three sets of permissions for three categories of users: owner, group, and others. Every file on Linux have their own owner and permissions.
There are 5 main parts on the listing: permission, owners, Dater, Size, Filename(You can see this using **ls -l** while your are on tilde)

Here's how permissions are represented and what they mean:

1. **Read (r)**: Allows users to view the contents of the file. For directories, it allows users to list the contents of the directory.
2. **Write (w)**: Allows users to modify the contents of the file. For directories, it allows users to create, delete, or rename files within the directory.
3. **Execute (x)**: Allows users to execute the file if it's a program or a script. For directories, it allows users to access (navigate into) the directory.

Permissions are set for three categories of users:

- **Owner**: The user who owns the file.
- **Group**: The group that the file belongs to.
- **Others**: All other users on the system who are not the owner or part of the group.

Permissions are represented in Linux with a 10-character string. The first character indicates the file type, followed by three sets of three characters each representing the permissions for the owner, group, and others, respectively.

For example, a permissions string might look like this: `-rwxr-xr--`.

- The first character `-` indicates it's a regular file. If it were a directory, it would be represented by `d`.
- The next three characters `rwx` represent the permissions for the owner.
- The next three characters `r-x` represent the permissions for the group.
- The last three characters `r--` represent the permissions for others.

To modify file permissions, you can use the `chmod` command. For example, to give the owner read, write, and execute permissions, you would use:

`chmod u+rwx filename`

To remove write permissions for others, you would use:

`chmod o-w filename`

And to set permissions recursively for all files and directories within a directory, you would use the `-R` option:
`chmod -R u+rwx directoryname`

Remember that changing file permissions can have security implications, so it's essential to understand who needs access to the file and what level of access they require.
#### ownership
- Ownership is the owner of the fil
- This have 2 kinds:User and Group
- To change the owner of file you can use the command
    **chown user:group {filename}

### CHOMD command
The `chmod` command in Linux is used to change the permissions of files and directories. It stands for "change mode". With `chmod`, you can modify the read, write, and execute permissions for the owner of the file, the group associated with the file, and other users.

The syntax of the `chmod` command is:

bashCopy code

`chmod [options] mode file(s)`

Here, `mode` specifies the new permissions you want to set, and `file(s)` specifies the file or files whose permissions you want to change.

The `mode` parameter can be expressed in two ways:

1. **Symbolic Mode**: Uses symbolic representations of permissions, which consists of three parts:
    
    - The target users: `u` for user/owner, `g` for group, `o` for others, `a` for all.
    - The operation to perform: `+` to add permissions, `-` to remove permissions, `=` to set permissions explicitly.
    - The permissions to change: `r` for read, `w` for write, `x` for execute.
    
    For example, to give the owner read and write permissions, you would use:
    `chmod u+rw filename`
    
2. **Numeric Mode**: Uses octal numbers to represent permissions. Each permission (read, write, execute) is assigned a value:
    
    - Read: 4
    - Write: 2
    - Execute: 1
    
    You sum these values to get the desired permissions. For example:
    
    - `777` gives read, write, and execute permissions to everyone.
    - `755` gives read, write, and execute permissions to the owner, and read and execute permissions to group and others.

Some common options for the `chmod` command include:

- `-R`: Recursively change permissions for files and directories within a directory.
- `-v`: Verbose mode, which shows the changes made.
- `-c`: Similar to verbose mode, but only displays changes made.

Here are a few examples:

- To give read and write permissions to the owner of a file:
    `chmod u+rw filename`
    
- To remove execute permissions from the group and others:
    `chmod go-x filename`
    
- To set permissions to 755 for a directory and all its contents recursively:
    `chmod -R 755 directoryname`
    

Remember to replace `filename` or `directoryname` with the actual names of the file or directory you want to modify.

- The parameter can be in numbers and symbols
    

1. Parameters in symbol
    

- chmod a+x filename   ->  adding execute permission for all  ( chmod +x filename)
    
- chmod u+x filename -> adding execute permission for user
    
- chmod g+x filename -> adding execute permission for group
    
- chmod o+x filename -> adding execute permission for other
    
- chmod -x filename -> removing execute permission for all
    
- chmod a+rwx , u-rw , g-x , o-xw filename -> gives rwx for all and removes something from all
    

B) Parameters in Number

- chmod 621 filename -> 6 for user, 2 for group, 1 for other  ( 6 = 4+2 ),  6 =r w
    
- chmod 777 filename -> 7 for users, 7 for group , 7 for others (7 =4+2+1),  7 = rwx
    