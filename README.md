# Onayiga TW Assignment
Technical writing assignment | HashiCorp interview

## Content

### What is the difference between push, pull, and fetch?

- `git push` - Sends changes from your local branch to a remote repository.
- `git fetch` - Receives changes from a remote repository, and copies them on to a tracking branch. This will not change your local branch.
- `git pull` - Receives changes from a remote repository, and merges them with the changes on your local branch.

This is how code is shared with a remote repository, you can think of it as "make the remote branch resemble my local branch". 
This will fail if the remote branch has diverged from your local branch: if not all the commits in the remote branch are in your local branch. 
When this happens, your local branch needs to be synchronized with the remote branch with git pull or git fetch and git merge.
`git fetch` again takes our current branch, and checks to see if there is a tracking branch. 
If so, it looks for changes in the remote branch, and pulls them into the tracking branch. 
It does not change your local branch. 
To do that, you'll need to do `git merge origin/master` (for the "master" branch) to merge those changes into your branch - probably also called "master".
`git pull` simply does a `git fetch` followed immediately by `git merge`. 
This is often what we desire to do, but some people prefer to use git fetch followed by git merge to make sure they understand the changes they are merging into their branch before the merge happens.
