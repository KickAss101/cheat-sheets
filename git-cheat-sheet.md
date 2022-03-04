<center><h2>Personal Git Cheatsheet</h2></center>

|Global Config|Description|
|--|--|
|git config --global user.name KickAss101|
|git config --global user.email jaswanthsunkara@protonamil.com|
|git config --global core.autocrlf input|input - linux \| true - windows|
|git config --global core.editor "codium --wait"|codium - vscodium \| code - vscode|
|git config --global -e|edit config file ~/.gitconfig|
|git config --global diff.tool codium|editor for comparing files in revisions|
|git config --global difftool.codium.cmd "codium --wait --diff $LOCAL $REMOTE"|configure difftool command|
|git config --global credential.helper store|stores creds in ~/.git-credentials|
|git config --global -l|displays all global config
---

|Useful Shortcuts|Description|
|--|--|
|git commit -am "msg"|Skip staging and commit
|git rm <file> --cached|unstage
|git status -s|Short status description
---
	
|Listing things|Description|
|--|--|
|git ls-files|Shows files in index|
|git ls-tree HEAD~*|Shows tree of specific commit|
|git stash list|Shows all stashes|
---

|Diffing|Description|
|--|--|
|git diff --staged|Displays changes btw index & commit
|git diff|Displays changes btw working tree & index
|git diff --name-status  main..<branch-name>|Displays what file will be affected
---

|Viewing logs, branches|Description|
|--|--|
|git log|Shows all commits meta data
|git log --oneline|Shows commit ID and comment
|git log --oneline --reverse|Shows commits in reverse order
|git log --oneline --stat|Shows changes in commits
|git log --oneline --all|Shows all branches
|git log <branch-name>|Shows all commits meta data in specified branch
---

|Viewing commits|Description|
|--|--|
|git show <commit-id> (or) <HEAD~*>|Shows commit info with diffing
|git show HEAD~*:<path>|Shows specific snapshot of file/directory
---
 
|Restore|Description|
|--|--|	
|git restore --staged (or) -S <file>|Restores file from commit to index, if no file in commit then file gets unstaged|
|git restore <file>|Restores file from index to worktree, if no file in index then file gets unstaged|
|git clean -fd|Removes untracked files|
|git restore --source=HEAD~* <file>|Restores file from specified snapshot to worktree, if no file in that snapshot then file gets deleted in the working tree|
|git restore --stagged --worktree|Restores file from commit to both working tree & index|
---

|Reset|Description|
|--|--|
|git reset|Reset current HEAD to the specified state| 
---

|Branching|Description|
|--|--|
|git branch|List avilable branches
|git branch <name>|Create new branch
|git branch -m <name> <new-name>|Rename branch
|git branch -D <branch-name>|Delete branch
---

|Stashing|Description|
|--|--|
|git stash push -m "msg"|Stores files besides index		 
---

<!-- |Github commands|Description|
|--|--|
|git fetch|Download objects and refs from another repository|
|git merge origin/master|Join two or more development histories together| -->








