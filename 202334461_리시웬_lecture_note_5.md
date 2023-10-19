# Linux CLI Lecture Note 2 (Lab 5)
# 202334461 리시웬  
---
# CLI
---
### I/O Redirection:   
##### 1. Standard Output
- By default, standard output is **screen**.
- You can redirect output **using “>”** after a command (e.g., ls) **to create and save the
output in a file**
- Command **“cat”** displays the content of a text file.
- **Using “>>”** appends **output to an extising file (if it already exitsts)**,
or **create and write to a new file** if it doesn’t exist.
##### 2. Standard Input
- By default, standard input is **from keyboard**.
- You can redirecct input from a file **using “<”.**
- **You can mix “<“ and “>” together** in a single line.
---
##### 3. Pipelines "|"
- Pipeline feeds **output of previous command to input of next command.**
- **Can be used continuously** ex)command1 | command2 | command3 | … 
- Press **"q"** key to exit the screen.
- When there are many files, **use wc -l**.
---
##### 4. Expansion
- Special characters expand its meaning when given to shell commands.
- **echo [comment]** : Print [comment]
- **echo** * : Print files in the current directory
- **echo ~** : Print files in the current user's home directory
---
##### 5. Tip 1: Backslash
- Backslah can be used to **ignore line change in command** (“enter”),
to **enter a long command in multiple lines**.
ex) ls -l \
---
##### 6. Permissions
- Linux is a **multi-user system**.
- Files and directories have **a permission assigned differently to owner / group / others.**
---
##### 7. Changing Permissions
- "chmod" changes permissions.
- -*rwx(1)rwx(2)rwx(3)* : 
*rwx(1)* - Read, write and execute permissions for the file owner.
*rwx(2)* - Read, write and execute permissions for the group owner fo the file.
*rwx(3)* - Read, write and execute permissions for all other users.

- ex) -rwxr-xr-x = 755 (The file's owner may read, write, and execute the file. All others may read and execute the file. This setting is common for programs that are used by all users.)
7 = 111 = rwx
6 = 110 = rw- for owner
0 = 000 = --- for group
0 = 000 = --- for others
- Change the permission of a file **“word.txt”** that only the owner (you) can read and write,
but all the others (including others in the group) can only read it. No execution is needed
for all users.
---
##### 8. Superuser
- A superuser has **all system administation authority.**
- Some commands need **superuser’s privilleges.**
- Put **“sudo”** before the command if you are a superuser.
---
##### 9. Text Editors
- In Linux, you can choose CLI-based or GUI-based text editors.
---
##### 10. Shell Script
- Write and run a shell script
ex) LISHIWEN myscript.sh
---
##### 11. Tip 2: History
- Type “history” to see previous command history.
- Or, save it to a text file.