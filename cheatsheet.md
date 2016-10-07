# Git Command Cheat Sheet

##### Cloning your remote directory
        git clone <remote directory>


##### Pulling down all branches in a remote repo, not just the default branch
        git fetch --all

##### Checking that status of your local repository - shows changed but not added files in red
		git status

##### Creating a new branch for you to work on
        git branch <new branch name>

##### See all branches in your remote repository
		git branch -a

##### Moving onto a branch
        git checkout <branch name>

##### Deleting a branch
		git branch -d <branch name>

##### Moving your changes to the staging area
        git add <file name>

##### Committing your changes
        git commit -m '<commit message here>'

##### Pushing your commit to the remote repository
        git push origin <branch name>

##### Creating a branch and moving onto it.
        git checkout -b <new branch name>

##### Merging changes from another branch, to your current branch
        git merge <branch you want to merge with your current branch>

##### Pulling remote changes into your local repo
        git pull origin <branch name>
        
##### Moving files while preserving git history
		git mv <source> <destination>
 
 
##### making a new branch whilst moving into it AT THE SAME TIME
		git checkout -b <new branch name>

