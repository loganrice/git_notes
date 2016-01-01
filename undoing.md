# Undoing

## Git Amend

Say you have just made a commit but a file has gotten
left out, like Gemfile.lock.  We can add that file to the 
previous commit with amend
  git commit --amend --no-edit

## Remove a file from staging

  git reset name_of_file
  
  I prefer an alias because reset doesn't quite fit the right terminology
  of what we are doing, at least in my mind.
  
  
