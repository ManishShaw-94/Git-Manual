# GIT MANUAL

> A **Git** is a distributed version control system used to track changes in files (open-source).

> **Github** is a cloud platform (by Microsoft) used to host Git repositories and collaborate on projects.

---------------------------

**Prerequisites (Windows):** Install Git and Gitbash

Verify Installation: git --version

**Connecting Git to GitHub (via SSH)**

**Steps to generate new SSH key (Linux / Git Bash):** 
```bash
ssh-keygen -t rsa -b 4096 -C "{your_github_email​@gmail.com}"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub
```
- Copy the output of the last command
- Add it to your GitHub/GitLab account under SSH Keys

---------------------------

### Basic Git Commands

--------------------------

**1. git init :** Initializes a new Git repository

**2. git status :** Shows the current state of files (staged, unstaged, untracked)

(In VS Code: U = Untracked files, M = Modified files)

**3. git branch {branch_name} :** Create a new branch (it creates a replica of the current head)

    a. git branch -a : List all branches (red color are remote branch and green color are local branch)

    b. git switch {branch_name} : Switch to another branch

    or git checkout {branch_name} : Another alternative to switch to another branch

    c. git checkout -b {branch_name} : Create and switch to a new branch

**4. git add {file_name} :** Stage a specific file

    a. git add . : Stage all changes

    b. git restore --staged {file_name} : Unstage a file

**5. git commit -m "{commit_message}" :** Save staged changes to the repository

    a. git reset --hard {commit_id}" : Revert to a specific commit
    
    b. git diff {commit_id}" : Show differences between commit and the latest commit

**6. git remote add {remote_name} {git_uri} :** Add a remote repository (usually named origin)

    a. git remote -v : List remotes

**7. git push :** Push changes to the remote repository

    a. git push -u {remote_name} master :** Push your changes to github repositories using command line 
    
    b. git push --set-upstream {remote_name} master : Push and set upstream (first time)

**8. git pull :** Fetch and merge changes from the remote repository

**9. git merge {source_branch}:** Merge another branch into the current branch (target branch).

**10. git log :**  View commit history

**11. git clone {git_uri} :** Download a repository from a remote source

**12. git stash :** Save work-in-progress changes temporarily

    a. git stash apply : Restore latest stash
    
    or git stash apply {stash_name}: Restore a specific stash
    
    b. git stash drop :** Delete a stash

    or git stash clear: Delete all stashes
    
    c. git stash list :** List all stashes
