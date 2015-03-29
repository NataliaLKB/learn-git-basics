# Introduction to Git and Version Control

This tutorial is targeted towards the students of Founders & Coders 8 week Coding Academy. Feedback or Suggestions (raised as an issue) or contributions (a pull request) are appreciated.

As a student, if you get stuck at any point, please open an issue and I will try to get back to you as soon as possible, or update the tutorial. If you would prefer, feel free to contact me on Gitter (search NataliaLKB).

The *introduction to Git* is aimed at the first week of the course. The hope is that this introduction will cover all you need to know to start collaborating on code with your fellow teammates.


# Contents
#### Introduction
1. [Need to Know Terminology](#terminology)
2. [Why Version Control](#version-control)
3. [Tutorial](#tutorial)
	* [Getting Started](#getting-started)
	* [Branching](#branching)
	* [Making Changes](#changes)
	* [Merging with Master](#merging)
	* [Merge Conflicts](#conflicts)
4. [Introducing Github Flow](#github-flow)


#### In Practice
- What you will need to get competent at by the end of the 8th week

1. More about feature branches
2. What is a commit?
3. About commit messages
4. When to add and commit?
5. How to merge commits together --> complex git 


# Introduction

This introduction to Git is aimed at first week students of [Founders & Coders](http://foundersandcoders.org/) 8 week coding academy. The hope is that this introduction will cover all you need to know to start collaborating on code with your fellow teammates. 


<a id="terminology" name="terminology"></a>
## Terminology

##### *Repository (repo)*
Simply put, this is your project folder. This repository can be located locally (in your file system on your computer), or remotely (on Github). Either way, it is the same repository.

##### *Version Control*
We will use Git for this. A way of keeping track of changes in the code which makes it possible to work with multiple developers on the same repo.

##### *Git*
A version control system.

##### *Github*
A remote location where you can store you code, and which all the members of the team have access to. Think of it like a dropbox for code. One of the big differences however is most repositories on github are public. Anybody can see your code.

##### *Commit*
A way of saving your code at different points along the project. Unlike many tools you may have used however, all commits are saved. This creates a project history and a way to track changes. 

##### *Branches*
As you work on a git repo the first branch you are on is usually the default branch. This is often called `master`. If you start working on a section of the website (say the footer styling), it is best practise to create your own branch for that feature. Creating your own branch is like taking a copy of `master` and renaming it. When you commit, they will now be on that new branch only. 

In the sections below we will walk through how to do this. For the meantime, just note that you always have one default branch, and can have as many other branches as needed.


<a name="version-control" id="version-control"></a>
## Why Version Control

##### Code Base History
Git can provide you with a complete history of every commit made on a project. Benefits include:

* Being able to see what differences to the file system you have made before you have commited.

* Being able to see what differences exist between commits

* Being able to move between difference commits (or places in time). This is especially useful if something became broken while you were working on it, and you need to start again.

In the introduction section of this tutorial, we won't be able to cover all these benefits in practise extensively. However, we will aim to give you all the information you will need to know by the end.

##### Multiple people working on the same files
Version control makes this possible. If you work on one file, and then I work on the same file at the same time when we want to combine our changes git allows us to keep both versions save that we can compare. This allows us to integrate our changes more swiftly. 

We will practice with this later.

##### Branching
A good work flow with git always involves branching. Having branches helps organise the code, and keep track of who is working on what.


<a name="tutorial" id="tutorial"></a>
## Tutorial

Before we begin, if you don't have a Github account, please get one.

Next please fork this repository.

![fork button on github](./img/fork.png)

On your local machine, please make sure you have git installed. If you are using a mac, please install with brew. Windows use http://git-scm.com/download/win. and Linux install using these instructions http://git-scm.com/download/linux.


<a name="getting-started" id="getting-started"></a>
### Getting Starting
The next step is to clone the forked version of this repository. Copy the url shown here: 
<picture of github repo>
Then use the command in your terminal:
    git clone <copied url>
Next, it is good to get in the habit after each command to use `git status`. Let us use it now. 
    git status
Now check which branch you are on:
    git branch
You should only see `master` which is the default branch in this repo.
For this tutorial, also use the command:
    git fetch --all
    git branch
Git fetch --all will fetch all the other branches in this repository, not just the default one.
You should see something like this in your terminal now:
<picture of terminal>
the branch name in green is the current branch you are on. In this case it is `master`.


<a name="branching" id="branching"></a>
### Branching
The next step is to create your own branch to work on. try this:
    git branch new-branch
It is best to try to name your branches as specific as possible, so not to confuse them with any others. There are many naming conventions out there for branches, but for this week simply try to name them off of a feature. For example (`navbar-collapse` or `sass-file-structure`). To see all your branches:
    git branch
As you can see, you have created your branch, but are not currently on it. To navigate onto it please:
    git checkout new-branch
    git branch
Now you can see you are on that branch. Go back to master and now we are going to delete `new-branch`.
    git checkout master    
    git branch -d new-branch
    git branch
As you can see, your branch is now gone. 


<a name="changes" id="changes"></a>
### Making Changes
Now it is time to make some changes in the project. Make yourself a new branch named `update-cheatsheet` and go onto it. open up the file cheatsheet.md in your favourite test editor (I would recommend sublime or atom. 
As you can see, this contains all the commands you will need to begin using git. Continue to add to it all the new commands you learn. To begin, here is a command that both creates a branch, and moves you onto it at the same time:
    git checkout -b <new branch name>
Add that command, and its description to cheatsheet.md and save it. Now in your terminal:
    git status
You will see something like this:
<picture of terminal>
You will see your changes in red. now we need to add them to the git staging area. Doing this is like telling git to pay attention to these files, and start tracking the changes. To do this write this command:
    git add cheatsheet.md
    git status
Now you can see the file name has turned green. Now to commit your changes.
    git commit -m 'adding new command in the cheatsheet'
    git status
The message could be anything, but it is best to make it something that describes what you just did.


<a name="merging" id="merging"></a>
### Merging Changes with Master
Now that you have made and committed your changes, it is time to merge your branch with master. Even though you are not working with anyone else on this repository, it is always good practice to make sure your current branch is completely up to date with master. Checkout back onto master and pull down. This command looks like this:
    git checkout master
    git pull origin master
Pulling down means that you are getting any recent changes from the remote master branch which is located in Github. Next go back to your branch (`update-cheatsheet`)  and merge with master.
    git merge master
Even though in this situation there isn't any changes to merge, it is best to get in the habit on going through these steps in your work flow. Merging like this means taking any possible changes in master and merging them with the branch you are currently on.
After you merge with master you have to push your changes to the remote repo (Github). 
    git push origin update-cheatsheet
Go to your browser and open up this repository in github. Press on branches, and then on PR
<pictures here>
Make a PR to master. Now merge, and delete your branch. 
<pictures here>
Return to your terminal and navigate to your local master branch. Pull down. You will see your branch update (fast-forward). delete the branch `update-cheatsheet`. 


<a name="conflicts" id="conflicts"></a>
### Merge Conflicts
Check all the branches on this repository. You will see a branch called merging-experiments. Checkout onto it and open up the git cheatsheet, as you can see there are some differences between this and master. To see these differences use command:
    git diff master
The differences in green and the additions on this branch, that don't exist on master. The red are the things that are on master, that don't exist on this branch.
Merge with master. You should have a git conflict that looks something like this:
<picture of merge conflict>
Do you see the lines at the top. The first section is labelled `HEAD` those are from this branch. The next section is from master. Delete the lines, and any other code you want until the cheatsheet looks like how you want it to look. 
Afterwards git status, add the files in red, commit, and push. Then make a PR to master like before and merge. Don't forget to update your local master branch, and delete the merged branch in Github and in your local repo. It is good to keep your working environments clean and organised. 

<a name="github-flow" id="github-flow"></a>
## Github Flow
Github flow is what most teams at Founders & Coders follow. It is simple and effective.

For a visual guide, and some helpful tips:
https://guides.github.com/introduction/flow/

To find out why Github uses Github flow:
http://scottchacon.com/2011/08/31/github-flow.html


More helpful RESOURCES:

http://gitreal.codeschool.com/
https://www.atlassian.com/git/tutorials/