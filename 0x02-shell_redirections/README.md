# 0x02. Shell, I/O Redirections and filters
## 0. Hello World
* Write a script that prints “Hello, World”, followed by a new line to the standard output.
### File: 0-hello_world
input : echo 'Hello, World'
## 1. Confused smiley 
* Write a script that displays a confused smiley "(Ôo)'.
### File: 1-confused_smiley
input : echo '"(Ôo)'\'
## 2. Let's display a file
* Display the content of the /etc/passwd file.
### File: 2-hellofile
input : cat /etc/passwd
## 3. What about 2?
* Display the content of /etc/passwd and /etc/hosts
### File: 3-twofiles
input : echo /etc/passwd /etc/hosts
## 4. Last lines of a file 
* Display the last 10 lines of /etc/passwd
### File: 4-lastlines
input : tail /etc/passwd
## 5. I'd prefer the first ones actually
* Display the first 10 lines of /etc/passwd
### File: 5-firstlines
input : head /etc/passwd
## 6. Line #2
* Write a script that displays the third line of the file iacta.
  * The file iacta will be in the working directory
  * You’re not allowed to use sed
input : head -3 iacta | tail -1
## 7. It is a good file that cuts iron without making a noise 
* Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.
### File: 7-file
input :
