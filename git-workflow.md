# Workflow

##
- Create a new branch locally for a specific feature
- Make changes to files
- Commit those changes to git
- Code review
- Merge those changes to master on Github
- Close out ('deleting') the feature specific branch (on GitHub & local)

**Using command line**
1. Navigate into the project root directory
  `git checkout -b <branch-name>`
  *Creates a new branch and changes to it*

**Using 'local' file browser & text editor**
2. Make changes to files & directories 'locally'
  *Test changes in browser if domain set-up to ensure correct*

**Using command line**
3. `git status` to check what has changed locally
4. `git add .` to add all files to staging area
  *If only certain files are to be added, then `git add <file-name>`*
5. `git commit -m "..."` to commit changes to git with a suitably descriptive message
6. `git push -u origin <branch-name>`
  *Pushes changes to remote repository with tracking set*
  *Authenticate with Github account if required*

**Go to [github.com/wesort](https://github.com/wesort)**
7. Project repository > Branches
8. Click 'New Pull Request' button
9. If necessary, change 'Base Fork' to the projects origin
  *Ensure correct branch (ie: `<branch-name>` is selected in dropdown)*
10. Click 'Create Pull Request' button
11. Click 'Merge Pull Request' button and then 'Confirm' button
12. Click 'Delete Branch' button
  *This removes the branch from Github (FYI: it's still in history)*

**Using command line**
13. `git status` for reassurance
14. `git checkout <master>` to move onto the '<master>' branch
  *Typically <master> is called "master", though on /whiteboard it's called "gh-pages"*
15. `git pull` to 'pull' down the changes to local that just occured during merge on Github
16. `git status` for reassurance
17. `git branch` to list active branches ('*' should be next to '<master>')
18. `git branch -d <branch-name>` to delete the branch locally
19. `git status` Only currently working branches should be listed
