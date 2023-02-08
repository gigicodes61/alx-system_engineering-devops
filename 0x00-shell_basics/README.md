# 0x00. Shell, basics
## 0. Where am I?
* Write a script that prints the absolute path name of the current working directory.
### File: 0-current_working_directory
input : pwd *(print working directory)*
## 1. What’s in there?
* Display the contents list of your current directory.
### File: 1-listit
input : ls *(list content)*
## 2. There is no place like home
* Write a script that changes the working directory to the user’s home directory
### File: 2-bring_me_home
input : cd ~
## 3. The long format
* Display current directory contents in a long format
### File: 3-listfiles
input : ls -l
## 4. Hidden files
* Display current directory contents, including hidden files (starting with .). Use the long format.
### File: 4-listmorefiles
input : ls -al
## 5. I love numbers
* Display current directory contents.
  * Long format
  * with user and group IDs displayed numerically
  * And hidden files (starting with .)
### File: 5-listfilesdigitonly
input : ls -lna
## 6. Welcome
* Create a script that creates a directory named my_first_directory in the /tmp/ directory.
### File: 6-firstdirectory
input : mkdir my_first_directory
## 7. Betty in my first directory
* Move the file betty from /tmp/ to /tmp/my_first_directory.
### File: 7-movethatfile
input : mv /tmp/betty /tmp/my_first_directory
## 8. Bye bye Betty
* Delete the file betty.
  * The file betty is in /tmp/my_first_directory
### File: 8-firstdelete
input : rm /tmp/my_first_directory/betty
