# Task 5.2 - Linux essentials  
  
***
  
## Analyzing `/etc/passwd/` & `/etc/group` system files  
  
#### `/etc/passwd` file contains the list of all system users and their attributes  
! screenshot of passwd file when I create test user to show its ID
The structure of each record is as follows.  
`:` is used for the separation of fields  
```
name: unique <user> name
x: password stored in /etc/shadow indicator
1000: unique user ID
1000: corresponding group ID
description: comment field that contains extra user information
/home/user: absolute path to user home directory
/bin/bash absolute path to command or shell
```
  
#### `/etc/group` file contains the list of all system groups and users, that belong to each of them  

> make table

0 root  
1 - 99 - predefined accounts
100 - 999 - reserved by system for system administrative and account groups
1000+ system users ID













  
#### Topic
**bold** *italics* `inline code`  
  
```
code
```
![img](./screenshots/img.png)  
  
  
***  
**Navigation:**  
*[Previous: Task 5.1](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1/blob/main/m5/task5.1/README.md)* | *[Next: Task 5.3](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1/blob/main/m5/task5.3/README.md)* | *[Task list](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1#1-task-list)*  
  
  
