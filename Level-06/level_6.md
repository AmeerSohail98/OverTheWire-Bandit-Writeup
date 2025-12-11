# Bandit Games (OTW)
## : &rarr; : Level - 6

### Problem description :
5. Solve level-6 challenge to get password for level-7 in the bandit war game?

![image](/Level-06/img1.png)

### Solution :
1. Login to the linux operating system

![image](/Level-06/img2.png)

![image](/Level-06/img3.png)

2. Using the following SSH command from the kali linux VM i connected to bandit page 

![image](/Level-06/img4.png)

3. After connection and providing password I am able to login to the bandit shell.

![image](/Level-06/img5.png)

4. Once logged in i used ls -la to check the files and directories available in the home. no files are directories are available.

![image](/Level-06/img6.png)

5. As per the problem statement The password is stored in 'somewhere on the server' so i started to check the linux file directory structure, First i started with /etc(etc-Edible text configuration) all the config files store here.

![image](/Level-06/img7.png)


6. So I just made an assumption that password would be stored in apache2 folder because it is a server related folder.

![image](/Level-06/img12.png)

7. I checked in the folder but there is no file available only config related files.
![image](/Level-06/img13.png)

8. Then i changed to other linux directory /usr where in this directory it contains user realted program, documentations and libraries so i thought because of the clue in the question that for the password file user is 'bandit7' and group owner is 'bandit6'.

![image](/Level-06/img15.png)

9. So i checked local directory, I thought may be different user files are stored there still unable to find the password file

![image](/Level-06/img16.png)

10. Then i changed to /var folder.And here instead of manual checking I used 'find' command to find out the file, I researched about find command whether it is possible to search with user name then i found a flag '-user' where we can use it to find the file that has a specific username.

### <ins> find . -type f -user bandit7 </ins>

![image](/Level-06/img17.png)
In the above image we can see that files belong to user bandit7 are displayed along with bandit7.password file. 

[ /Var - The "variable" data directory, which stores files whose content is expected to change continually during normal system operation.]

11. So i changed to the folder where that file is located.  

![image](/Level-06/img18.png)

12. Once i changed to the folder againg i used to filter the exact file usin file command with grep command to filter out the text file.

### <ins> find . -type f -user bandit7 -exec file '{}' + | grep 'ASCII text' </ins>

![image](/Level-06/img19.png)

![image](/Level-06/img20.png)

13.Then used cat command with \ escape sequence in between the .(dot) to read it as file name, Then i got output.

![image](/Level-06/img21.png)