# Bandit Games (OTW)
## : &rarr; : Level - 5 

### Problem description :
5. Solve level-5 challenge to get password for level-6 in the bandit war game?

![image](/Level-05/img1.png)

### Solution :
1. Login to the linux operating system

![image](/Level-05/img2.png)

2. Using the following SSH command from the kali linux VM i connected to bandit page 

![image](/Level-05/img3.png)

3. After connection and providing password I am able to login to the bandit shell.

![image](/Level-05/img4.png)

4. Once logged in i used ls -la to check the files and directories available in the home. After that i used 'cd' command  to change to the directory inhere the again used ls -la to list out all normal and hidden files it displayed so many directories.

![image](/Level-05/img5.png)

![image](/Level-05/img6.png)

5. So in this many directories it will take so much time to find out particular command so i researched in file command in the ubuntu manual an i found one command where we can iterate through all the folders at once.

![image](/Level-05/img7.png)

6. So i used this command to check out all the files type at once in previous level also we used same type of command with some modification then i got all the files data type.
### <ins>find . -type f -exec file '{}' /;</ins>

![image](/Level-05/img7_2.png)

![image](/Level-05/img8.png)

![image](/Level-05/img9.png)

7. The file datatype is displayed but still they are not displayed in proper organized way where we can find them easily so here i used 'du' command to check the size of data to get some insights but  here also all the files memory size is mostly displayed same.

![image](/Level-05/img10.png)

![image](/Level-05/img11.png)

![image](/Level-05/img12.png)

![image](/Level-05/img13.png)

8. So i tried a flag called Exclude for the file command to exclude ASCII file type with very long lines data but it didn't work and I got error.

![image](/Level-05/img14.png)

![image](/Level-05/img15.png)

9. So the command i last used in previous level to get all files data i used it here to get a better oraganized understanding of file data type and architecture, so the output is displayed in proper organized way.

### <ins>find . -type f -exec file '{}' + | grep 'ASCII text' </ins>
Additionaly i used grep to highlight the ascii text data files.

![image](/Level-05/img16.png)

10. So after checking the proper data format i listed some folders that stand out in those directories.

![image](/Level-05/img17.png)

11. So finally used cat command to check all of the files data at a time by providing all directories path and got the key from 'maybehere10' folder and    '.file2'

![image](/Level-05/img18.png)

![image](/Level-05/img19.png)


