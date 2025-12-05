# Bandit Games (OTW)
## : &rarr; : Level - 3 

### Problem description :
3. Login to the bandit page using ssh from our attack machine?

![image](/Level-03/img0.png)

### Solution :
1. Login to the linux operating system

![image](/Level-03/img1.png)

2. Using the following SSH command from the kali linux VM i connected to bandit page 

![image](/Level-03/img2.png)

3. After connection and providing password I am able to login to the bandit shell

![image](/Level-03/img3.png)


4. Once able to login I used ls, ls -la commands to check for files and after that i found a folder called 'inhere' so to double check i used file command on that and displayed the following output.

![image](/Level-03/img4.png)

5. I used cd command to chage into that 'inhere' directory and Checked the directory using ls -la command it displayed me all hidden files and the file we are searching for, so i used PWD command to know my current directory path and tried to used that with cat command as i did in previous level but got error, So i tried to check the file type using file command i got error because there is some space in between the file name.

![image](/Level-03/img5.png)

6. So did some research on file name spacings we can use either '\' escape sequence for white space or quotes to enclose the file name so that command can read it as a single file name so i tried with \ but i got error because of dot(.) presence so when ised quotes i got the key to next level 

### <ins> cat "...Hiding-From-You" </ins>

![image](/Level-03/img6.png)
