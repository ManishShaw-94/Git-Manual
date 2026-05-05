# DOCKER MANUAL

> A **Git** is a version control tool to track file changes (open-source)
> (In VS Code, U = Untracked changes, M = Modified)

> **Github** is a platform allows you to host git repositories (microsoft product).

---------------------------

**Pre-requisite (Windows):** Install Git and Gitbash

Verify Git Installation: git --version

**Connecting Git to Github account:** Using SSH key

### Steps to generate new SSH key locally using linux: 
  1. ssh-keygen -t rsa -b 4096 -C "{your_github_email@gmail.com}"
  2. eval "$(ssh-agent -s)"
  3. ssh-add ~/.ssh/id_rsa
  4. cat ~/.ssh/id_rsa.pub
       (then copy the content)
  5. Copy and paste the ssh key on Github/Gitlab
--------------------------

---------------------------

### Basic Git Commands

--------------------------

**1. git init :** Initialize a git repository

**2. git status :**  

**3. git branch {branch_name} :** To create a new branch (create a replica of the current head)

    a. git branch -a : To list all branch (red color are remote branch and green color are local branch)

    b. git switch {branch_name} : To change your current branch

    or git checkout {branch_name} : To change your current branch

    c. git checkout -b {branch_name} : Creates a new branch and switch into that branch automatically

**4. git add {file_name} :** Staging the changes

    a. git add . : To stage all files

    b. git restore --staged {file_name} : Remove changes from stagging

**5. git commit -m "{commit_message}" :** Commiting the changes which has been staged

    a. git reset --hard {commit_id}" : Revert back to that specific commit

    b. git diff {commit_id}" : Difference between that specific commit and the latest commit

**6. git remote add {remote_name} {git_uri} :** Add a remote repository to the local repository (note: generally "origin" is the name of the remote)

    a. git remote -v : 

**7. git push :** Push your changes to github repositories

    a. git push -u {remote_name} master :** Push your changes to github repositories using command line 

    b. git remote -b : 
    
    c. git push --set-upstream {remote_name} master : when you push for the first time

**8. git pull :** Commiting the changes which has been staged

**9. git merge {source_branch}:** Merging source branch to target branch locally (make sure you are currently in your target branch).

**10. git log :**  Logging all the commits

**11. git clone {git_uri} :** To clone repositories from internet

**12. git stash :** To save the work in progress changes

    a. git stash apply : To bring back the wip changes
    
    or git stash apply {stash_name}: To bring back a specific stash changes
    
    b. git stash drop :** To delete the wip changes one by one

    or git stash clear: To delete all the stash at once
    
    c. git stash list :** To list all the stashes
