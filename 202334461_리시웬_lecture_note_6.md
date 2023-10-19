# Linux CLI Lecture Note 3 (Lab 6)
# 202334461 리시웬  
---
### Version Control and Collaboration
- It’s essential to use a version control system for software development
and other documentation works.
- Basic solution: *Making copies*
    ex) 프로젝트_최종.txt
        프로젝트_최종_수정1.txt
        프로젝트_최종_수정1_진짜최종.txt
        프로젝트_최종_수정1_진짜최종_추가수정2.txt
        .
        . 
        .
- We need a **systematic management system** for version control and collaboration.
---
### Changes vs. Snapshots
##### changes
- Storing data as *changes to the base version* 
ex)
File A ---> A1 -----> A2
File B -------------> A1 ---> A2
File C ---> A1 ---> A2 -----> A3
##### Snapshots
- Storing data as *snapshots*
ex)
File A ---> File B ---> File C
A1 ---> B ---> C1
A1 ---> B ---> C2
A2 ---> B1 ---> C2
---
### Local, Centralized, and Distributed Version Control
##### 1. Local
File -> version 3 - version 2 - version 1
##### 2. Centralized
Computer A <- version 3 - version 2 - version 1 -> Computer B
##### 3. Distributed
Server Computer(version 3 - version 2 - version 1) <---> Computer A(version 3 - version 2 - version 1) <---> Computer B(version 3 - version 2 - version 1)

---
### Three Staes in Git
**Modified**(working Directory) ---Stage Fixes--> **staged**(Staging Area)
**staged**(Staging Area) ---Commit--> **Comitted**(git directory(Repository))
**Comitted**(git directory(Repository)) ---Checkout the project --> **Modified**(working Directory) 
---
### Installing Git
- Linux / Mac / Windows (check pre-installed version)
- Linux (install on a Debian-based distribution)
- Mac (https://git-scm.com/download/mac)
- Windows – Run “Git Bash” (https://git-scm.com/download/win)
---
### Git config: First-time setup
1. **System level**: --system option. Affects all uses and repositories on the system (administrative)
file: /etc/gitconfig
2. **Global (user) level**: --global option. Affects all repositories of a current user
file: ~/.config/git/config
3. **Local level**: --local option. Specific to the current repository
file: .git/gitconfig

**Each level overrides values in the previous level: system -> global -> local**

---
- **Initializing a Repository** in an Existing Directory : *$ git init*
- **Checking Repository Status** : *$ git status*
- **Adding a new file** to be staged (tracked) : *$ git add [file_name]*
- **Adding all files** to be staged (tracked) : *$ git add .*
- **Unstaging a file** : *$ git rm –cached [file_name]*
- **Ignoring a file** : 
 1. ignore all .a files : *.a
 2. but do track lib.a, even though you're ignoring .a files above : !lib.a
 3. only ignore the TODO file in the current directory, not subdir/TODO: /TODO
 4. ignore all files in any directory named build : build/
 5. ignore doc/notes.txt, but not doc/server/arch.txt : doc/*.txt
 6. ignore all pdf files in the doc/directory and any of its subdirectories : doc/** /*.pdf
- **Commit** : *$ git commit -m “commit message”*
- **Change branch name** : *$ git branch*