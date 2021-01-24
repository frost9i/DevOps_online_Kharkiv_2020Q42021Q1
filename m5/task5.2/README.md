# Task 5.2 - Linux essentials  
  
***
  
## Analyzing `/etc/passwd/` & `/etc/group` system files  
  
#### `/etc/passwd` file contains the list of all system users and their attributes  
`:` is used for the separation of fields  
![etc passwd](screenshots/passwd.png)  
The structure of each record is as follows.  
| Field | Description |
| :---: | --- |
| vmuser | unique \<user\> name |
| x | password stored in `/etc/shadow` indicator |
| 1001 | unique user ID |
| 1001 | corresponding group ID |
| ` ` | comment field that contains extra user information |
| `/home/vmuser` | absolute path to user home directory |
| `/bin/bash` | absolute path to user command or shell |
  
Working system includes many users, that can be distinguished by their IDs:  
| ID range | User classification |
| :---: | --- |
| 0 | `root`, the most privileged system user |
| 1 - 99 | predefined accounts (system daemons, pseudousers) |
| 100 - 999 | reserved by system for system administrative and account groups |
| 1000+ | regular users IDs |
  
  
#### `/etc/group` file contains the list of all system groups and users, that belong to each of them  
![etc group](screenshots/group.png)  
The structure of each record is as follows.  
| Field | Description |
| :---: | --- |
| vmgroup | unique \<group\> name |
| x | can store encrypted password |
| 1002 | unique group ID |
| vmuser | users that belong to the group |
User that have this group as their primary in `/etc/passwd` do not have to be included.  
  
  
## About UID and GID  
UID - User IDentity  
GID - Group IDentity  
  
User and Group identification numbers are set upon creation in iterative manner, meaning that each new created user will have *+1* to his ID compared to the last created user.  
  
User can be created with a specified UID using following command:  
`sudo useradd -u 2001 -m vmuser2`  
where `-u 2001` sets the value of UID, that can be checked using  
`id -u vmuser2`  
  
The same goes to GID, each newly created group takes unoccupied group ID,
or it can be manually set using following command:  
`sudo groupadd -g 2002`  
  
Manual definition of UID and GID allows creating user or group with any ID, even in 1 - 999 range. If the ID is already taken the system message will appear:  
`useradd: UID 1 is not unique`  
  
***
  
#### How to determine if user belongs to a specific group?  
There're many utilities to perform this task. Some require installation, but I prefer methods that are already on board:  
```
getent group vmgroup
```
The reverse lookup command to determine groups that user is in:  
```
id vmuser
id -Gn vmuser
```
  
#### How to add user to the system and what parameters to use?  
```
sudo useradd <username>
sudo passwd <username>
```
Additional options can be included, like:  
`-m` - create home directory, if doesn't exist;  
`-M` - don't create home directory if it is set to create homedir by default;  
`-u` - set specific UID;  
`-s` - define specific user shell, e.g. `/bin/zsh`;  
`-p` - set password in CLI;  
`-g` - define main group user is in;  
```
sudo useradd -m -u 2002 -s /bin/zsh testuser
```
  



### Scripting  


to do:



  
***  
**Navigation:**  
*[Previous: Task 5.1](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1/blob/main/m5/task5.1/README.md)* | *[Next: Task 5.3](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1/blob/main/m5/task5.3/README.md)* | *[Task list](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1#1-task-list)*  
  
  
