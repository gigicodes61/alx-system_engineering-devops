# 0x03. Shell, init files, variables and expansions
## 0. <o>
* Create a script that creates an alias.
  * Name: ls
  * Value: rm *
### File: 0-alias
input : alias ls="rm *"
## 1. Hello you
* Create a script that prints hello user, where user is the current Linux user.
### File: 1-hello_you
input : echo "hello $USER"
## 2. The path to success is to take massive, determined action
* Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.
### File: 2-path
input : export PATH=$PATH:/action
## 3. If the path be beautiful, let us not ask where it leads
* Create a script that counts the number of directories in the PATH.
### File: 3-paths
input : echo $PATH | tr ":" "\n" | wc -l
## 4. Global variables
* Create a script that lists environment variables.
### File: 4-global_variables
input : printenv
## 5. Local variables
* Create a script that lists all local variables and environment variables, and functions.
### File: 5-local_variables
input :  
