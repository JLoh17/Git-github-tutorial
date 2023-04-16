# Git & Github tutorial

Git is a distributed version control system

Commits are like a save

The main branch of the repository is called **master branch**
A branch is a copy of a repository at a certain point of time that has different changes

Repositories (or repos) are the containers for git.
Anytime you want to use git on a project (for tracking and committing of changes), you need to initialise a repository with `git init`

## Git command lines

### Linux Command lines

`clear` - clears CLI <br>
`ls` - list all files in current directory (similar to dir) <br>
`pwd` - (present working directory); current file path <br>
`cd <folder>` - change directory <br>
`cd ..` - goes back one folder up <br>
`mkdir <folder name>` - creates folder <br>
`touch index.html` - creates index.html file

\* Note that some of the command lines are different for windows

### Starting off

`git init` - makes the current folder a git repository locally and everything will now be tracked by git <br>
`touch index.html` - create files in current folder (if you don't open via VS Code) <br>
`git add <file1 file2 etc.>` - adds file to staging area <br>
`git add .` - add all files <br>
`git commit -m <insert commit message>` - the message should be descriptive and be less than 50 characters <br>
`git status` - check the status of your repo/changes <br>
`git merge master` - adds whatever is on master branch to your branch, but still keeps your stuff (master branch is not updated). This means you need to git add . e.g.

### Git history

`git log` - shows the history of commits done, also shows the commit hash (highest is most recent)

### Branching

`mkdir <branchname>` - makes a new folder <br>
`git branch` - shows the branches, \* shows which branch you're in <br>
`git branch <name of new branch>` - creates a new branch <br>
`git checkout -b <name of new branch>` - creates and move to new branch (-b means make a new branch) <br>
`git checkout <name of branch>` - changes to new branch <br>
`git branch -d <name of branch>` - deletes that branch <br>
`git branch -m oldName newName` - change branch name

### Connecting to Github

`git remote add origin <url>` - links a remote repository to your repository using the name origin <br>
`git remote -v` - shows remotes you are linked to <br>
`git remote remove origin` - unpairs remote link

### Pushing/pulling

`git push origin master` - pushes to the remote repository <br>
`git push origin <branch-name>` - pushes the branch to the repository <br>
`git pull origin master` - pulls from the remote repository <br>
`git fetch origin` - updates branches <br>
`git remote prune origin` - clears deleted branches

`git checkout <hash number from git log>` - reverts back to old commit

### Stashing

Stashing - Git provides an easy way of stashing uncommitted changes so that we can return to them later, without having to make unnecessary commits. (Mainly done when we are working on a branch, we need to jump to another branch but don't want to commit it yet)

`git stash` - stash changes that we want to come back to later. It takes all uncommitted changes (stage or unstaged) and stashes them, reverting the changes to before. You can stash multiple times. <br>
`git stash pop` - re-apply to recently stashed changes to your working copy <br>
`git stash apply <stash-id>` - apply whatever is stashed away without removing it from the stash. <br>
`git stash list` - view all stashes
`git stash drop <stash-id>` - drops a particular stash
`git stash clear` - clear out all stashes

#### Notes

\* Note that git <> is not needed to be typed

Fork allows you to copy someone’s a repo to your own GitHub (takes exact current state); note that it says that it has been forked. This allows you permission to change the repo however you want, push them up (make sure you linked the repo). If you want to props changes, submit a pull request.

## Linking Git to Github

1. Create a new repository in Github (keep the tab open)
2. Open VSCode and…
3. Create a folder for your project
4. Type `git init` in the terminal
5. Copy the git remote command from GitHub (the SSH link). Should start with `git remote add origin git@github.com...`
6. `git remote -v` to check we have correct address and alias
7. `git push origin master` in git
8. Refresh repo on in GitHub
