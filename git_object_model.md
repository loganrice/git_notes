#Git Object Model

## Git directory

Name | Function
--- | ---
HEAD | a pointer to the currently checked out object
objects/ | where git stores representations of all files, directories, and commits
refs/ | where git stores branches, tags, remotes, etc.

## Blobs
Git uses blobs to track files. The blob stores only the content
of the file not the name.
To look at the contents of a blob use the first 8 characters of the 
blog object name
  $ git cat-file -p 3b18e512


## Trees
A git object that contains a list of pointers to blobs and other trees.


## Commit
A commit file contains
* hash of current working tree
* hash of parent commit(s) (except for root commits which do not have parents)
* author info and date
* commiter info and date
* full commit message

![diagram]
(https://thoughtbot-images.s3.amazonaws.com/upcase/git-course/git-base-object-model.png)
