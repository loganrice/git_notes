#Stash

## Git Stash
  git stash -u
  > -u will include untracked files
  > this is usually the behavior we want. 
  > if we do not include -u only the tracked files 
  > will be stashed.

### Git Stash Drop
  git stash drop
  > removes a created stash

### Git Stash Pop
  git stash pop
  > adds the top most stash back and removes it
  > essentially doing git stash apply && git stash drop   
  > git stash apply alone does not remove the stash

## Git RefLog
  git reflog
  git reflog show name_of_single_branch
  > a list of every change, merge, etc ever made
  > the reflog is local to your machine only.
  > in other words it's only tracking your activity.


