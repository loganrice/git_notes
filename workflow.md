# Workflow

## Start with new branch
```
$ git checkout -b new_feature
```
make your changes

## Push to github
push local branch to github and use the -u to setup tracking.
we will be creating a pull request in the next step.
```
$ git push -u origin
```

## Create a pull request
Try to break pull requests up into refactoring changes or feature changes.
```
git pr
```

## Make any needed changes per pull request comments

## Rebase for Fast Forward Merge
Once we're ahead of master, we can perform an interactive rebase to revise our
commits and craft our history. In particular, we can use this time to squash
down cleanup and WIP commits, ensuring that each commit we keep is useful and
has a solid commit message.

```
$ git rebase -i master
```
within the text editor replace "pick" with "s" on all of the 
commits you wish to squash.
push your changes.

## Close Pull Request
```
$ git co master
$ git merge -
# Since we've made sure to rebase, this will inherently be a fast-forward merge,
# but we can use the --ff-only flag to ensure this. Also, the - refers to the
# last checkout branch.
$ git push

```
## Delete branch
delete local feature branch
```
$ git branch -d <branchName>
```

## Delete Remote Branch
* **option 1** 
```
$ git push origin --delete <branchName>
```
* **option 2** We can delete the branch via the GitHub PR page, and then git pull on master,
letting the fetch prune setting automatically clean up our local reference to
the remote branch.

