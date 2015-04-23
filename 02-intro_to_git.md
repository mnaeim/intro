# Intro to Git

##git branch
A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. Think of them as a way to request a brand new working directory, staging area, and project history. New commits are recorded in the history for the current branch, which results in a fork in the history of the project. The git branch command lets you create, list, rename, and delete branches. It doesn't let you switch between branches or put a forked history back together again. For this reason, git branch is tightly integrated with the git checkout and git merge commands.

##git status
The git status command displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven't, and which files aren't being tracked by Git. 

##git add
The git add command adds a change in the working directory to the staging area. It tells Git that you want to include updates to a particular file in the next commit. However, git add doesn't really affect the repository in any significant way-changes are not actually recorded until you run git commit.

###Parameters:
 * `-p` : Interactively choose hunks of patch between the index and the work tree and add them to the index. This gives the user the chance to review the difference before adding modified contents to the index.

##git commit
This is one of the most important Git commands. The git commit command commits the staged snapshot to the project history. Committed snapshots can be thought of as "safe" versions of a project. Git will never change them unless you explicity ask it to. Snapshots are committed to the local repository.

###Parameters: 
 * `-m` : This command makes you write a summary or a message for the changes you have made before pushing it. 

##git fetch
The git fetch command imports commits from a remote repository into your local repo. The resulting commits are stored as remote branches instead of the normal local branches that we've been working with. This gives you a chance to review changes before integrating them into your copy of the project.

##git push
Pushing is how you transfer commits from your local repository to a remote repo. It's the counterpart to git fetch, but whereas fetching imports commits to local branches, pushing exports commits to remote branches.

##git pull
It is a shortcut for git fetch followed by git merge. Basically, it runs git fetch with the given parameters and then git merge merges the retrieved branch into the curent branch.

##git merge 
Merging is Git's way of putting a forked history back together again. The git merge command lets you take the independent lines of development created by git branch and integrate them into a single branch.

##git checkout
The git checkout command lets you navigate between the branches created by git branch. Checking out a branch updates the files in the working directory to match the version stored in that branch, and it tells Git to record all new commits on that branch. Think of it as a way to select which line of development you're working on. Also, The git checkout command serves three distinct functions: checking out files, checking out commits, and checking out branches. In this module, we're only concerned with the first two configurations. Checking out a commit makes the entire working directory match that commit. This can be used to view an old state of your project without altering your current state in any way. Checking out a file let you see an old version of that particular file, leaving the rest of your working directory untouched.

