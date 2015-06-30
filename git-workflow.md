# Workflow

##
- Creating a new branch locally for a specific feature
- Making changes to files
- Committing those changes to git
- Merging those changes to master on Github
- Closing out ('deleting') the feature specific branch

*On the command line*
1. Navigate into a suitable directory
  `git checkout -b <branch-name>`
  Creates a new branch and changes to it

*Switch to 'local' file browser & text editor*
2. Make changes to files & directories 'locally'

*Switch to command line*

3. `git status` to check what has changed locally
4. `git add .` to add all files
  - If only certain files are to be added, git add <file-name>
5. `git commit -m "..."` to commit changes to git with a suitably descriptive message
6. `git push -u origin <branch-name>`
  - Pushes changes to remote repository
  - Authenticate with Github account if required

*Switch to [github.com/wesort](https://github.com/wesort)*

7. Project repository > Branches
8. Click 'New Pull Request' button
9. If necessary, change 'Base Fork' to the projects origin
  - Ensure correct branch (ie: `<branch-name>` is selected in dropdown
10. Click 'Create Pull Request' button
11. Click 'Merge Pull Request' button and then 'Confirm' button
12. Click 'Delete Branch' button
  - This removes the branch from Github, but it's still in history

*Switch to command line*

13. `git status` to ensure / reassurance
14. `git checkout master` to move onto the 'master' branch
15. `git pull` to 'pull' down the changes to local that just occured during merge on Github
16. `git status` to ensure / reassure
17. `git branch` to list active branches ('*' should be next to 'master')
18. `git branch -d <branch-name>` to delete the branch locally
