# Task 5.1 - Linux essentials  
  
***
  
## Part 1. - #  
  
Being logged it as 'root' user can perform any system commands without using \>sudo modifier.  
Root is better not to be used with password authentication.  
Changing root password:
```
passwd  
```
Changing \<user\> password as `root`:  
```
passwd <user>  
```
Encrypted passwords are stored in *\/etc\/shadow* in a form of hash:  
```
root:*LOCK*:14600::::::
adm:*:18313:0:99999:7:::
ec2-user:$6$KcUtT2Dd$LtF27FeXUNvW3wMHgQjkeS9ONub1m30zq5.k.D7Q7hXyYrTPHKKgs8qM1VlbfgDyXYsj1yOoY.HByydRfYLZm0:18638:0:99999:7:::
```
In the example `&6&` stands for SHA-512 algorithm.  

  
  
  
  
  
  
  
  
  
    
***  
**Navigation:**  
*[Previous: Task 4.4](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1/blob/main/m4/task4.4/README.md)* | *[Next: Task 5.2](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1/blob/main/m5/task5.2/README.md)* | *[Task list](https://github.com/frost9i/DevOps_online_Kharkiv_2020Q42021Q1#1-task-list)*  
  
  
