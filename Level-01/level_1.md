# Bandit Games (OTW)
## : &rarr; : Level - 1 

### Problem description :
2. Login to the bandit page using ssh from our attack machine?

![image](/Level-1/img1.png)

### Solution :
1. Login to the linux operating system

![image](/Level-1/img2.png)

2. Using the following SSH command from the kali linux VM  i connected to bandit Level-1 page 

![image](/Level-1/img3.png)

3. After connection and providing password I am able to login to the bandit shell

![image](/Level-1/img4.png)
![image](/Level-1/img4_2.png)

4. Once able to login I used ls, ls -l, ls -a commands to check for files.

![image](/Level-1/img5.png)

5. Then used file commands to check the file data type able to check for all files except '-'.

![image](/Level-1/img5.png)

6. So I checked all other files data using cat command to get any clues for how to access the '-' file data.

![image](/Level-1/img6.png)
![image](/Level-1/img6_2.png)

7. After some research to view data of this type of particular files we can use complete file path with cat command like this 

### <ins> cat /home/bandit1/- </ins>

![image](/Level-1/img7.png)

By using the above command i am able to view the data of the file for next level.