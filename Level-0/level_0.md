# Bandit Games (OTW)
## : &rarr; : Level - 0 

### Problem description :
1. Login to the bandit page using ssh from our attack machine?

![image](/Level-0/problem.png)

### Solution :
1. Using the following SSH command from my kali linux VM  i connected to bandit Level-0 page 

![image](/Level-0/login.png)

In this command -p is port instruction to connect with particular port of external(remote) machines.

2. After connection and providing password I am able to login to the bandit shell

![image](/Level-0/user.png)

3. Once logged in I ls command to check for files one 'readme file' is there so I used to cat to check the file data and got flag for next level.
Level-0 -----> Level-1

![image](/Level-0/flag.png)