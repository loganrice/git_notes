#Craft History

# Add Patch
  git add --patch

  allows you to choose individual blocks of code within staged
  files to commit.

Key | Operation
--- | ---
h | display list of available keys and their operation
y | stage the current hunk
n | skip this hunk
s | split the hunk
a | stage this and all remaining hunks
q | quit, skipping all remaining hunks
e | edit the hunk manually, 

## Cherry Pick

helps moves commits to another branch. For example,
if you make changes to master but really meant
to make changes on a feature branch you can
move those commits to the feature branch.

  git diff origin/master..master
  # check to make sure your changes are there

  git checkout some_branch
  git cherry-pick origin/master..master

If you do the above operation your commits will still be on 
the master branch. 
  git checkout master
  git reset --hard origin/master

## Rebase

Done from the context of your feature branch specify the target branch
to rebase onto. For example 
  $ git branch
    *feature_branch
    master
  $ git rebase master


## Squashing

You can use interactive rebase to squash commits to create 
a cleaner and better commit history

For example, from the feature branch
  git rebase -i master

within the text editor replace "pick" with "s" on all of the 
commits you wish to squash.
