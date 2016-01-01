## Git Log
  git log
  git log --oneline
  git log --oneline --decorate
  git log --oneline --decorate --graph --all
  
  > as you can see the arguments can become long and a pain to type
  > we can create an alias. We will call it sla for "short log all"
  git config --global alias.sla 'log --oneline --decorate --graph --all'

## Searching Git Log
  git --grep
  git -E (extended regular expressions)
  git -i (case insensitive) 
  
  > for example if you wanted to search all of the logs for
  > any commit with the word cache or caching
  git -E -i --grep 'cach(e|ing)'
