# Git Command Cheat Sheet

##### Cloning your remote directory
		git clone <remote directory>

##### Checking that status of your local repository
		git status

##### Creating a new branch for you to work on
		git branch <new branch name>

##### Create and move to new branch
		git checkout -b <new branch name>

##### See all branches in your remote repository
		git branch -a

##### Moving onto a branch
		git checkout <branch name>

##### Deleting a branch
		git branch -d <branch name>

#### Creates a branch, and moves you onto it
 		git checkout -b <new branch name>

#### commit changes
git commit -m 'comment'

#### pull original file to have latest version of file from github so that you and your team are working with the latest changes
git checkout master
git pull origin master

#### Merge with master
git merge master

#### Push changes to remote repo on github
git push origin update-cheatsheet

#### Creates a branch, and moves you onto it at the same time
 		git checkout -b <new branch name>
