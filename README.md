# git-alias

Simple aliases for git.

To install:
```
git clone https://github.com/0xc00010ff/git-alias &&
cd git-alias &&
make install
```
To verify, run `git aliases`

- `a` : `add`  
Add a file to the index
- `amend` : `commit --amend`  
Add currently staged changes to the previous commit (or just rename the previous commit)
- `aliases` : `config --get-regexp alias`  
List all aliases  
- `b` : `branch`  
List current branches  
- `ball` : `branch --all`   
List all branches, including remote copies
- `brnach` : `branch`  
Common typo for branch
- `c` : `commit`  
Commit everything from the index into git history
- `clear` : `!clear && ls && git status`  
A clean git status
- `co` : `checkout`  
Point to a different branch
- `d` : `diff`  
See the current unstaged (red) changes since last commit
- `drop` : `checkout --`  
Delete the unstaged (red) changes
- `f` : `fetch`  
Only fetch the current branch from upstream (but no merge)
- `graph` : `log --oneline --graph --decorate`  
Pretty git logs
- `last` : `log HEAD~1..HEAD --oneline`  
Print the last commit
- `lastdiff` : `diff HEAD~1 HEAD`  
Show the difference between the last commit and the one before
- `list` : `log --oneline`  
A condensed form of the commit log
- `mastiff` : `log --oneline master..HEAD`  
Compare commits between this branch and master  
- `new` : `checkout -b`  
Compare commits between this branch and master  
- `pr` : Some heady bash script... view source for details
Creates a pull request off the current branch. Make sure you pushed first!  
- `pullrequest` : Some heady bash script... view source for details
Long form for the above.  
- `remaster` : `! _current=$(git branch | sed -n -e "s/^\* \(.*\)/\1/p") && git checkout master && git pull && git checkout $_current && git rebase master`  
This one is heavy. Pop over to master, pull, pop back to the current branch and rebase master. You might want to stash first.
- `rename` : `branch -m`  
Rename the current branch
- `s` : `!clear && ls && git status`  
A clean git status, same as **clear**
- `stage` : `add`  
Add files to the staging area (green)
- `unamend` : `reset --soft HEAD@{1}`  
Undo the amend you just did, if you did one
- `uncommit` : `reset HEAD~1 --soft`  
Reset the previous commit's changes back into the staging area (green)
- `unstage` : `reset`  
Move changes out of the stage (green) into the working area (red)
