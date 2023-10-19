# Linux CLI Lecture Note 1 (Lab 4)
# 202334461 리시웬  
---
# Linux
![](https://velog.velcdn.com/images/lijahong/post/f0ae8d8c-fac9-458a-a5c5-3ef6e6bcbbfe/image.png)
## 1. Linux explanation
- The photo above is the mascot of Linux, a penguin.  Released by Linus Torvalds in 1991.  
- Linux is **open source unix-like operating systems and kernels**.  
- Most widely-used platform for open source software development.  
- Linux has **excellent security** and **allows installing or updating software on a server while it is turned on** without the need for a new boot.
- Runs on **CLI(Command Line Interface)**, but many distributions support **GUIs** as well.
---
## 2. Kernels and Shell
 - Kernel: Core of OS that **controls and communicates with hardware resource**.  
 - Shell: Interface that **allows users to communicate with kernel**: bash, zsh, ...
 Users runs applications and give commands through shell.  


 - Most users **communicate with the kernel through an interface called the shell**.  
 - Shell is **an interface tool** that the user directly encounters on the screen and delivers commands.  
 ---
## 3. CLI(Command Line Interface) vs GUI(Graphical User Interface)  

### CLI
- Work by entering **commands directly** using the **keyboard**.
- Relatively **fast**
- Scripts enable automation and records
- Basic environment for **developers**

##### VS

### GUI
- Method of **selecting menus** mainly using the **mouse**
- Relatively **low**
- Manual labors required for repetitive tasks
- For **daily users**
---

## 4. Shell command
##### 1. pwd
- ***pwd***: Shows the current path in a hierarchical directory
##### 2. cd and ls
- ***cd***: change directory
- ***ls***: list files and directories
~~~
    ls /bin         |   List the files in the /bin directory (or any oter directory we care to specify)
    ls -l           |   List the files in the working directory in long format
    ls -l /etc /bin |   List the files in the /bin directory and the /etc directory in long format
    ls -la . .      |   List all files (even ones with names beginning with a period character, 
which are normally hidden) in the parent of the working directory in long format
~~~
##### 3. arguments
- ***/*** : root (top directory)
- ***.*** : current directory
- ***. .*** : upper-level directory
- ***~*** : home of current user
- ***/[directory name]*** : absolute path
- ***./[directory name]*** : relative path
- ***. ./[directory name]*** : relative path
##### 4. options
- ***-l*** : show detailed information (long format)
- ***-lh*** :  same as above, but size in units
##### 5. Tip
- ***Autocompletion*** : press "tab" key
- ***past commands*** : press "up arrow" key
- ***clear*** : clear commands
##### 6. Manipulation 
 !Warning - These commands may delete or overwrite your files and directories! Make sure to backup your important contents.  
1. ***cp*** : copy files and directories
2. ***mv*** : move files and directories or rename them
3. ***rm*** : delete files and directories *permantely and irreversevely* **!Caution** Try it with ls first
4. ***mkdir*** : make a new directory
5. ***wildcards***
~~~
    *           |   All filenames
    g*          |   All filenames that begin with the character "g"
    b*.txt      |   All filenames that begin with the character "b" and end with the characters".txt"
    Data???     | All filenames that begin with the characters "Data" followed by exactly 3 more characters
~~~
##### 7. help
- ***help or man [command]*** : Use when you want to know the desired function or detailed information.
##### 8. exit
- ***exit*** : close the terminal.