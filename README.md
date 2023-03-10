# Onayiga TW Assignment
Technical writing assignment | HashiCorp interview

## Content

### What is the difference between push, pull, fetch, and merge Git commands?

The following information describes common commands used in Git, and details how these commands allow you to share code with a remote repository.

- `git push` - Sends changes from your local branch to a remote repository.
- `git fetch` - Receives changes from a remote repository, and copies them on to a tracking branch. This will not change your local branch.
- `git merge` - Aligns and merges missed commits from a remote repository with your local branch. 
- `git pull` - Receives changes from a remote repository, and merges them with the changes on your local branch.

If any commits from the remote repository do not make it to your local branch, a divergence will occur and will result in an error. To fix this, sync your local branch with the remote branch on the repository by using the `git merge origin/master` command. This  merges any missed changes from your local branch with the changes on the master branch.

`git fetch` again takes our current branch, and checks to see if there is a tracking branch. 
If so, it looks for changes in the remote branch, and pulls them into the tracking branch. 
It does not change your local branch. 
To do that, you'll need to do `git merge origin/master` (for the "master" branch) to merge those changes into your branch - probably also called "master".
`git pull` simply does a `git fetch` followed immediately by `git merge`. 
This is often what we desire to do, but some people prefer to use git fetch followed by git merge to make sure they understand the changes they are merging into their branch before the merge happens.
