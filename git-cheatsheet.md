# Git Command Cheatsheet
  - local = device working on (ie June 2015: Webfaction server)
  - remote = Github repository / repo

##### Initialising a new repository for git
  - Done once in the root of the project
  - This makes git aware of the files
    `git init`

##### Cloning your remote directory
    `git clone <remote directory>`

##### Checking that status of your local repository
    `git status`

##### View existing remotes
    `git remote -v`

##### Add remote repository (Github)
  - owner = wesort
  - repo = [project-title]
    `git remote add origin https://github.com/owner/repo.git`

##### Retrieve any changes from remote (add to local)
  - ensure on correct branch
    `git pull`

##### Pulling down all branches in a remote repo, not just the default branch
    `git fetch --all`

##### Creating a new branch for you to work on
    `git branch <branch-name>`

##### See all branches in your remote repository
    `git branch -a`

##### Moving onto a branch
    `git checkout <branch-name>`

##### Creating a branch and moving onto it
    `git checkout -b <branch-name>`

##### Deleting a local branch
    `git branch -d <branch-name>`

##### Moving a single file's changes to the staging area
    `git add <file name>`
    
##### Moving ALL changes to the staging area
    `git add .`

##### Committing your changes
    `git commit -m "<commit message here>"`

##### Pushing your commit to the remote repository
  - Sets tracking information for future pulls
  - ref: http://stackoverflow.com/a/5697856/1515623
    `git push -u origin <branch-name>`

##### Creating a branch and moving onto it.
    `git checkout -b <branch-name>`

##### Merging changes from another branch, to your current branch
    `git merge <branch you want to merge with your current branch>`

##### Pulling remote changes into your local repo
    `git pull origin <branch name>`

##### Prints out project history regardless of where one is in the timeline
    `git reflog`
    
##### Prints out all previous commits
    `git log`
