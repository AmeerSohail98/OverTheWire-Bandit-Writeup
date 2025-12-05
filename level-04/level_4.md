# Bandit Games (OTW)
## : &rarr; : Level - 4 

### Problem description :
4. Solve level-4 challenge to get password for level-5 in the bandit war game?

![image](/Level-04/img1.png)

### Solution :
1. Login to the linux operating system

![image](/Level-03/img1.png)

2. Using the following SSH command from the kali linux VM i connected to bandit page 

![image](/Level-04/img2.png)

3. After connection and providing password I am able to login to the bandit shell.

![image](/Level-04/img3.png)

4. Once logged in i used ls -la to check the files and directories available in the home. After that i used 'cd' command  to change to the directory inhere the again used ls -la to list out all normal and hidden files it displayed so many files in the directory.

![image](/Level-04/img4.png)

5. I used 'du' command to check out the sizes of file so maybe to get a clue by using file names and brace extensions to check multiple files disk usage together but still i got the error. Then i used '--' argument with -(hyphen) filename then i got the disk usage of the file.

![image](/Level-04/img5.png)

6. Then i researched in google to check disk usage of multiple files together in a single command so i found out a command of mixed flags for the 'du' as follows.

### <ins>du -ah</ins>

![image](/Level-04/img6.png)

where du = disk usage; <br>
      a  = all files; <br>
      h  = Human readable;

7. Then i thought is there a way to gather all of the data from the files into one single file collected, Then after some research i got a command.

![image](/Level-04/img7.png)

### <ins>cat /home/bandit4/inhere/* > output_file.txt</ins>

8. Here i used cat command with file directory path with (*)wildcard with redirection operator to create a new text file with the data, But still got the error as permission denied.

![image](/Level-04/img8.png)

9. Then i used file command to check each and every file data individually then i am able to find out that file 7 consist the ASCII-text data. 

![image](/Level-04/img9.png)

10. So again i thought what if there is more than ten files i can't do them manually so  researched about file and got a combination command with the file so i tried and able to find out the data type of all files in the output.

![image](/Level-04/img10.png)

### <ins> find . -type f -exec file {} + </ins>

where find = to find out files
       .   = present directory <br>
    -type f= to provide file type
    -exec  = to execute the command
     file  = file command to know the data type
     {} +  = empty place holder to replace the file name and + is used to move to the next file.

11. And finally used  cat command with directory path to find out the data hidden in te file.

### <ins>cat /home/bandit4/inhere/-file07</ins>
      
![image](/Level-04/img11.png)
