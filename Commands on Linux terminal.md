To change the default shell of the user (example to change to zsh)
+ `chsh -s /bin/zsh john`
To get more information about the user we created 
+ ***cat /etc/passwd***
To make visible the user you created using useradd(By default it is not visible on /home)
+ ***sudo mkhomedir_helper {username}***
How to login into the other user that are created
+ *** sudo su - {username}***
+ to exit just type **exit** and press enter



