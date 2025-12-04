# Bandit Games (OTW)
## : &rarr; : Level - 2 

### Problem description :
2. Login to the bandit page using ssh from our attack machine?

![image](/Level-02/img1.png)

### Solution :
1. Login to the linux operating system

![image](/Level-02/img2.png)

2. Using the following SSH command from the kali linux VM  i connected to bandit Level-1 page 

![image](/Level-02/img3.png)

3. After connection and providing password I am able to login to the bandit shell

![image](/Level-02/img4.png)
![image](/Level-02/img5.png)

4. Once able to login I used ls, ls -l, ls -a commands to check for files.

![image](/Level-02/img6.png)

5. Checked the current directory using PWD command.

![image](/Level-02/img7.png)

6. Like in level-2 tried to provide full directory path in file name and tried to read the data but error displayed in the output.

![image](/Level-02/img8.png)

![image](/Level-02/img9.png)

7. Tried the "./"  for the file directory path with cat command but still error generated like this

![image](/Level-02/img10.png)

8. Using -- Argument: The -- argument is a common convention in many commands to signify the end of options. Anything following -- is treated as a non-option argument, including dashed filenames, So i tried and checked with this still got error.

![image](/Level-02/img11.png)

9. The error generated because of spaces so to Escape the spaces used backslash (`\`) in the command with the -- argument using cat command then i got the output from that spaces file like below

### <ins> cat -- --spaces\ in\ this\ filename-- </ins>

![image](/Level-02/img12.png)