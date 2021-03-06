# pwdone

### Password manager with a command-line interface

pwdone is a multi-user, multi-platform command-line utility for storing and organizing passwords and another info for
logins

### Contents
1\. Common commands

2\. Installing and unistall the utility

3\. Backup and restore data
1. Common commands
   
   help on using the utility:
   ```
   $ pwdone --help
   ```
   
   more detailed help on using utility commands:
   ```
   $ pwdone [command] --help
   ```  

   adding a new user:
   ```
   $ pwdone uadd
   ```
   or using options:
   ```
   $ pwdone uadd -u user-name
   ```      

   adding a new record in passwords DB:
   ```
   $ pwdone add
   ```
   or using options:
   ```
   $ pwdone add -u user-name -l login-for-site -n record-name
   ```  

   show all user records:
   ```
   $ pwdone show
   ```  

   get the password of record to the clipboard:
   ```
   $ pwdone get
   ```
   or using options:
   ```
   $ pwdone get -n record-name
   ```  

   full list of command options:
   ```
   $ pwdone [command] --help
   ```

2. Installing the utility
    1. Installing on Ubuntu
       <br/>
       <br/>
       pwdone works in the X Window System
       <br/>
       <br/>
       the utility requires python 3.8 or higher

       check version python:
       ```
       $ python3 --version
       ```
       install pip3:       
       ```
       $ sudo apt update
       $ sudo apt upgrade
       $ sudo apt install python3-pip
       $ pip3 --version
       ``` 
       install pwdone:       
       ```
       $ sudo apt install -y xclip
       $ git clone https://github.com/vakhnin/pwdone.git
       $ cd pwdone
       $ pip3 install --user .
       $ echo -e "export PATH=\"$HOME/.local/bin:$PATH\"" >> ~/.bashrc
       $ source ~/.bashrc
       ``` 
       uninstall pwdone:       
       ```
       $ pip3 uninstall -y pwdone
       $ pip3 uninstall -y -r uninstall_list.txt
       ```              

    2. Installing on Windows  
       
        the utility requires python 3.8 or higher<br> 
        check version python:
        ```
        > python --version
        ```      
        check pip3:
        ```
        > pip3 --version
        ```     
         install pwdone:
         ```
         > git clone https://github.com/vakhnin/pwdone.git
         > cd pwdone
         pwdone> pip3 install .
         ```  
         uninstall pwdone:        
         ```
         pwdone> pip3 uninstall -y pwdone
         pwdone> pip3 uninstall -y -r uninstall_list.txt
         ```
       
3. Backup and restore data
   <br>
   <br>
   All data is stored in the database.sqlite file. 
   You can simply copy the database.sqlite file for 
   backup and replace the database.sqlite file with 
   the one you previously saved to restore all data.
   
   Show where is BD file:
   ```
   $ pwdone where
   ```   