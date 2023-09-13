# Git Guide

## Command line git

- status
  - Shows statu of the local repository. This status includes:
    - number of local commits that have not been synced with remote (GitHub)
    - list of files in local folder than are NOT being tracked by git
    - list of files in local folder that have changes that need to be committed
    - `git status`
- clone 
  - copies or "clones" a github respository from a url for tracking on a local system. Example: `git clone git@github.com:WSU-kduncan/ceg3120-MuhammedAbu.git`
    - must generate ssh key pair using `ssh-keygen -t ed25519 -C "your_email@example.com"` in you local system.  Then copy the pulic key from the folder it was generated into and paste it into your github settings under ssh key pair. 
- add
  - add a file or folder for tracking. 
  - Example: `git add foo.txt` Furthermore, you can use `git add *` to track all unadded files/folders. 
- rm
  - removes a file or folder for tracking.
  - Example: `git rm generic-file.txt`
- commit
  - commits an added file for tracking. Must be done before pushes tracked file to remote (github) repository. Can add an update message.
  - Example: `git commit foo.txt` then enter message 
    - Or use `git commit -a -m "deleted unneeded text"` to commit all already tracked files and type the message into the command line for quicker use.
    - To change or update a commit message after already committing use `git commit --amend` then change message. 
- push
  - pushes any tracked and committed files to github repo. Example: ` git add foo.txt`.. 
- fetch
  - The git fetch command downloads objects to the local machine without overwriting existing local code in the current branch. Ex. `git fetch`
- merge
  - Git merging combines sequences of commits into one unified history of commits. 
    - For example you can create a new branch `hotfix` and create any neccasry changes/commits and when you want to merge those changes back to the `main` branch you can use `git merge hotfix`. 
- pull
  - Pulls any changes you made from the remote github repo to the local system. Example: `git pull` will pull any and all created and edited files and adds/replaces     - them to your local repo. 
- branch
  - creates a new git branch Example: `git branch` then you can name the branch. To see branches you can use `git branch -r` or `git show-tree` (need to install `git-
  - extras` to use this command).
- checkout
  - `git checkout` command lets you navigate between the branches created by git branch.
    -  If you have a branch named `hotfix` for example you can switch to it by using `git chechout hotfix`.
- init
  - `git init` initilaizes or "creates" a git repository and should be the first thing used before starting a project using a git repo, since without it git commands will not be available.
    - If you want to clone an initialized repo from a remote system, use `curl ipinfo.io` to get the ip of the user, then use `git clone user@ip:relative-path-to-repo.git` in local system. *Note: The remote system has to have a public key that matches the private key of the local system.
    - If `git clone` was used then `git init` is not needed and the directory the git repo was cloned into is already initialized and ready to go.
    - remote
  - `git remote` The git remote command lets you create, view, and delete connections to other repositories.

## git files & folders

Provide descriptions of expected contents and what these are used for

- .git folder
  - Should contain all the information neccasry for your git repo function and opearet properly like metadata, object database, commit log, branch data, etc. 

- .gitignore file
  - should have all the files/folders in your repository that you want to be ignored for tracking. Can ignore all files in a directory using `*` and you can omit         -certain files that would've been ignored using `!`. 
- ~~.git/hooks~~

## GitHub

Provide basic how-to-use guides for both.  This should be short and sweet so that you can refer to it as a quick guide.

- Pull requests
  - Let others knnow what changes/commits used made and that you are ready to merge changes to main. 
- SSH authentication to repositories
  - must generat ssh key pair using `ssh-keygen -t ed25519 -C "your_email@example.com"` in you local system. Then copy the pulic key from the folder it was generated into and paste it into your github settings under ssh key pair.Then you can use `git clone git-repo-url` to clone onto local system.  
- ~~Actions~~

## Resources
Other resources are welcome, just cite them (you can do lazy citations here, or use markdown to make links throughout your guide)

- [Pro Git Book](https://git-scm.com/book/en/v2)
- https://learngitbranching.js.org/?locale=en_US - interctive guide
- https://rogerdudler.github.io/git-guide/ - simple guide


