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

# Cherry Pick

helps moves commits to another branch. For example,
if you make changes to master but really meant
to make changes on a feature branch you can
move those commits to the feature branch.

  git diff origin/master..master
