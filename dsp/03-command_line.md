# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > 
history  gives a list of all previous commands     
!!       repeat previous command.    

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`.    
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > 
ls      lists files           
ls -a   lists all files including hidden files (long list)           
ls -l   lists files with permissions, timestamps, size    
ls -lh  similar to ls -l but the file size has unit suffixes, not just bytes        
ls -lah long list of files with unit suffixes      
ls -t   list files by time modified   
ls -Glp long list of files enabling color output and writes a slash after each file if it is a directory   


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 
ls -lrt list by reverse date--oldest first  
ls -d   displays only directories  
ls -1   lists files on a separate line   
ls -R   lists files and subdirectories   
ls -g   long list of files without the owner name  



---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > 
Xargs reads data from standard input (stdin) and executes the command (supplied to it as an argument) one or more times based on the input read. 

Example:   
find . -name "*.c" | xargs rm 

This finds filenames in the current directory that end in .c and pipes it through to the xargs rm command which removes them.
 

