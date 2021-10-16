# Git Cheatsheet
Below are the most useful **terminal** and **Git commands** used in the Git.

## Bash/Terminal Basics

 **Make a new folder (aka make directory)**
`
 $  mkdir <FOLDERNAME>
`

**Navigate into an existing folder (aka 'change directory')**
`
 $ cd <FOLDERNAME>
`

 **List the items in a folder**
`
 $ ls
`


## Configuring Git

**Check Git version**
`
 $  git --version
`

**Set your name**
`
 $  git config --global user.name "Your Name"
`

**Set your email**
`
 $  git config --global user.email youremail@example.com
`

**Set your Github account (case sensitive)**
`
 $  git config --global user.username uSeRnAmE
`


## Git Basics

 **Turn Git on for a folder**
`
 $  git init
`

**Check status of changes to a repository**
`
 $ git status
`

 **View changes to files**
`
 $ git diff
`

 **Add a file's changes to be committed**
`
 $ git add <FILENAME>
`

 **To add all files changes**
`
 $ git add .
`

 **To commit (aka save) the changes you've added with a short message describing the changes**
`
 $ git commit -m "your commit message"
`

 **Copy a repository to your computer**
`
 $ git clone <URL>
`


## Git Branches

 **Create a new branch**
`
 $  git branch <BRANCHNAME>
`

**Move onto a branch***
`
 $ git checkout <BRANCHNAME>
`

**You can create and switch to a branch in one line**
`
 $ git checkout -b <BRANCHNAME>
`

**List the branches**
`
 $ git branch
`

**Rename a branch you're currently on**
`
 $ git branch -m <NEWBRANCHNAME>
`


## Git Remotes

 **Add remote connections**
`
 $  git remote add <REMOTENAME> <URL>
`

**Set a URL to a remote**
`
 $ git remote set-url <REMOTENAME> <URL>
`

 **View remote connections**
`
 $ git remote -v
`


## Pulling in Git

**Pull in changes**
`
 $  git pull
`

**Pull in changes from a remote branch**
`
 $ git pull <REMOTENAME> <REMOTEBRANCH>
`

 **See changes to the remote before you pull in**
`
 $ git fetch --dry-run
`


## Push & Merge in Git

**Push changes**
`
 $  
git push <REMOTENAME> <BRANCHNAME>
`

 **Merge a branch into current branch**
`
 $ git merge <BRANCHNAME>
`


## Deleting Remotes and Branches in Git

**Delete a local branch**
`
 $  git branch -D <BRANCHNAME>
`


**Delete a remote branch**
`
 $ git push <REMOTENAME> --delete <BRANCHNAME>
`

