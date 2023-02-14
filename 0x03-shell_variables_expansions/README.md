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
input : set
## 6. Local variable
* Create a script that creates a new local variable.
  * Name: BEST
  * Value: School
### File: 6-create_local_variable
input : BEST="School"
## 7. Global variable
* Create a script that creates a new global variable.
  * Name: BEST
  * Value: School
### File: 7-create_global_variable
input : exoprt BEST="School"
## 8. Every addition to true knowledge is an addition to human power
* Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.
### File: 8-true_knowledge
input : echo $(($TRUEKNOWLEDGE + 128))
## 9. Divide and rule
* Write a script that prints the result of POWER divided by DIVIDE, followed by a new line. 
  * POWER and DIVIDE are environment variables
### File: 9-divide_and_rule
input : echo $((POWER / DIVIDE))
## 10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath
* Write a script that displays the result of BREATH to the power LOVE
  * BREATH and LOVE are environment variables
  * The script should display the result, followed by a new line
### File: 10-love_exponent_breath
input : echo $((BREATH**$LOVE))
## 11. There are 10 types of people in the world -- Those who understand binary, and those who don't
* Write a script that converts a number from base 2 to base 10.
  * The number in base 2 is stored in the environment variable BINARY
  * The script should display the number in base 10, followed by a new line
### File: 11-binary_to_decimal
input : echo $((2#$BINARY))
## 12. Combination
* Create a script that prints all possible combinations of two letters, except oo.
  * Letters are lower cases, from a to z
  * One combination per line
  * The output should be alpha ordered, starting with aa
  * Do not print oo
  * Your script file should contain maximum 64 characters
### File: 12-combinations
input :
