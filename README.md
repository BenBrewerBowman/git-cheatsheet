# Git Cheatsheet



## Basic Commands

##### View both staged and unstaged files
`git status`

##### Add file/s to be committed
`git add .` (adds all files) <br>
or  <br>
`git add <filename>` (adds specific file) <br>

##### Commit to git
`git commit -m "<commit msg>"`

##### Update previous commit message: 
`git commit --amend -m “<new msg>”`

##### Reset to remote HEAD
`git reset HEAD`

##### Reset a file to version at HEAD
`git checkout HEAD -- <filename>`

##### Reset local master to look exactly like remote head
`git checkout master && git reset --hard origin/master`



## Branching

##### Check out a different branch
`git checkout <branch name>`

##### Create a new branch and check it out
`git checkout -b <branch name>`

##### Rename a git branch
`git branch -m <oldname> <newname>"`

##### View list of remote branches
`git fetch --all`

##### Update list of remote branches
`git remote update origin --prune`

##### Pulls remote branch and checks it out
`git fetch origin <branchName>	&& git checkout <branchName>`

##### Delete remote branch
`git push origin --delete <branchName>`



## Altering Commit History

##### Smashes last number of commits into one commit with a new message
`git reset --soft HEAD~<#OfCommits> && git commit -m “<msg>”`

##### Repo reverts back to the state of the previous commit
`git reset HEAD~<Xnum>`                  

##### Add more commits to the last commit and change the git message
`git add <all files to commit> && git commit --amend -m “<new msg>”`

##### Remove previous commit (removes all changes as well)
`git reset --hard HEAD~1`

##### Back-in commit to a previous commit
`git cherry-pick <commit #>`



## Viewing Changes to Files
##### Follow changes to a file
`gitk <filename>`

##### Follow changes to a file including past renames
`gitk --follow <filename>`

##### show entire history of a file (including beyond renames and diffs for all changes)
`git log --follow -p -- <filename>`

##### show changed files under git, without knowing the entire file path
`git log -- */<filename>.<file extension>`



## Other
##### Go back in time to a state before a git command (like before a rebase or merge)
`git reflog`
`git reset --hard <commit #>`

##### Remove a file from being tracked by git
`git rm --cached <file name>`

