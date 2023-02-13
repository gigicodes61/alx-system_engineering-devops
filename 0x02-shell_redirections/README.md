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
input : echo "Best School" > \\\*\\\\"'\"Best School\"\\'"\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)
## 8. Save current state of directory
* Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.
### File: 8-cwd_state
input : ls -la > ls_cwd_content
## 9. Duplicate last line
* Write a script that duplicates the last line of the file iacta
  * The file iacta will be in the working directory
### File: 9-duplicate_last_line
input : tail -n 1 < iacta >> iacta
## 10. No more javascript
* Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.
### File: 10-no_more_js
input : find . -type f -name "*.js" -delete
## 11. Don't just count your directories, make your directories count
* Write a script that counts the number of directories and sub-directories in the current directory.
  * The current and parent directories should not be taken into account
  * Hidden directories should be counted
### File: 11-directories
input : find . -type d -not -name '.' | wc -l
## 12. What’s new
* Create a script that displays the 10 newest files in the current directory.
 * Requirements:
  * ne file per line
  * Sorted from the newest to the oldest
### File: 12-newest_files
input : ls -t1 | head
## 13. Being unique is better than being perfect
* Create a script that takes a list of words as input and prints only words that appear exactly once.
  * Input format: One line, one word
  * Output format: One line, one word
  * Words should be sorted
### File: 13-unique
input : sort | uniq -u
## 14. It must be in that file
* Display lines containing the pattern “root” from the file /etc/passwd
### File: 14-findthatword
input : grep -i "root" /etc/passwd
## 15. Count that word
* Display the number of lines that contain the pattern “bin” in the file /etc/passwrd
### File: 15-countthatword
input : grep -i "bin" /etc/passwd | wc -l
## 16. What's next? 
* Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.
### File: 16-whatsnext
input : grep -iA 3 "root" /etc/passwd
## 17. I hate bins
* Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.
### File: 17-hidethisword
input : grep -v "bin" /etc/passwd
## 18. Letters only please
* Display all lines of the file /etc/ssh/sshd_config starting with a letter.
  * include capital letters as well
### File: 18-letteronly
input : grep -i "^[a-z]" /etc/ssh/sshd_config
## 19. A to Z
* Replace all characters A and c from input to Z and e respectively.
### File: 19-AZ
input : tr "A" "Z" | "c" "e"
## 20. Without C, you would live in hiago
* Create a script that removes all letters c and C from input.
### File: 20-hiago
input : tr -d "Cc"
## 21. esreveR
* Write a script that reverse its input.
### File: 21-reverse
input : rev
## 22. DJ Cut Killer
* Write a script that displays all users and their home directories, sorted by users.
  * Based on the the /etc/passwd file
### File: 22-users_and_homes
input : cut -d':' -f1,6 /etc/passwd | sort
## 23. Empty casks make the most noise
* Write a command that finds all empty files and directories in the current directory and all sub-directories.
  * Only the names of the files and directories should be displayed (not the entire path)
  * Hidden files should be listed
  * One file name per line
  * The listing should end with a new line
  * You are not allowed to use basename, grep, egrep, fgrep or rgrep
### File: 100-empty_casks
input : find . -empty | rev | cut -d '/' -f 1 | rev
## 24. A gif is worth ten thousand words
* Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories.
  * Hidden files should be listed
  * Only regular files (not directories) should be listed
  * The names of the files should be displayed without their extensions
  * The files should be sorted by byte values, but case-insensitive (file aaa should be listed before file bbb, file .b should be listed before file a, and file Rona should be listed after file jay)
  * One file name per line
  * The listing should end with a new line
  * You are not allowed to use basename, grep, egrep, fgrep or rgrep
### File: 101-gifs
input : find -type f -name "*.gif" | rev | cut -d "/" -f 1 | cut -d '.' -f 2- | rev | LC_ALL=C sort -f
## 25. Acrostic
* An acrostic is a poem (or other form of writing) in which the first letter (or syllable, or word) of each line (or paragraph, or other recurring feature in the text) spells out a word, message or the alphabet. The word comes from the French acrostiche from post-classical Latin acrostichis). As a form of constrained writing, an acrostic can be used as a mnemonic device to aid memory retrieval.
Create a script that decodes acrostics that use the first letter of each line.
  * The ‘decoded’ message has to end with a new line
  * You are not allowed to use grep, egrep, fgrep or rgrep
### File: 102-acrostic
input :
