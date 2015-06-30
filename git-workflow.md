# GitFlow - ie: GitHub Workflow
- Create a new branch locally for a specific feature
- Make changes to files
- Commit those changes to git
- Code review
- Merge those changes to master on Github
- Close out ('deleting') the feature specific branch (on GitHub & local)

#### Using command line
1. Navigate into the project root directory
  - `git checkout -b <branch-name>`
  - *Creates a new branch and changes to it*

#### Using 'local' file browser & text editor
1. Make changes to files & directories 'locally'
  - *Test changes in browser if domain set-up to ensure correct*

#### Using command line
1. `git status` to check what has changed locally
2. `git add .` to add all files to staging area
  - *If only certain files are to be added, then `git add <file-name>`*
3. `git commit -m "..."` to commit changes to git with a suitably descriptive message
4. `git push -u origin <branch-name>`
  - *Pushes changes to remote repository with tracking set*
  - *Authenticate with Github account if required*

#### Go to [github.com/wesort](https://github.com/wesort)
1. Project repository > Branches
2. Click 'New Pull Request' button
3. If necessary, change 'Base Fork' to the projects origin
  - *Ensure correct branch (ie: `<branch-name>` is selected in dropdown)*
4. Click 'Create Pull Request' button
5. Click 'Merge Pull Request' button and then 'Confirm' button
6. Click 'Delete Branch' button
  - *This removes the branch from Github (FYI: it's still in history)*

#### Using command line
1. `git status` for reassurance
2. `git checkout <master>` to move onto the '<master>' branch
  - *Typically <master> is called "master", though on /whiteboard it's called "gh-pages"*
3. `git pull` to 'pull' down the changes to local that just occured during merge on Github
4. `git status` for reassurance
5. `git branch` to list active branches and * should be next to \<master>
6. `git branch -d <branch-name>` to delete the branch locally
7. `git status` Only currently working branches should be listed