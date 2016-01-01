# Log

## Git Log
  git log
  git log --oneline
  git log --oneline --decorate
  git log --oneline --decorate --graph --all
  
  > as you can see the arguments can become long and a pain to type
  > we can create an alias. We will call it sla for "short log all"
  git config --global alias.sla 'log --oneline --decorate --graph --all'

## Searching Git Log commits
  git --grep
  git -E (extended regular expressions)
  git -i (case insensitive) 
  
  > for example if you wanted to search all of the logs for
  > any commit with the word cache or caching
  git -E -i --grep 'cach(e|ing)'

## Searching Git Log code
  git log -S example_method
  > this will search commits for anytime we added or removed a 
  > call to example_method

## File Specific Git Log
  git log --oneline  -- name_of_file
  
  git blame --online -- name_of_file
  > checks the most recent commit for every line of the file
  > and who made the changes.

## Reset changes to last commit
  git checkout .


## Undo a Commit

Remove a commit from history and revert to the point where
the files were staged, right before the commit happened.

  git reset --soft HEAD^

  or create an alias
  git config --global alias.uncommit 'reset --soft HEAD^'
