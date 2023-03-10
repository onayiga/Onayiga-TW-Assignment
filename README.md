# Onayiga TW Assignment
Technical writing assignment | HashiCorp interview

## Content

### What is the difference between push, pull, fetch, and merge Git commands?

The following information describes common commands used in Git, and details how these commands allow you to share code with a remote repository.

- `git push` - Sends changes from your local branch to a remote repository.
- `git fetch` - Gets changes from a remote repository, and copies them on to a tracking branch. This does not change your local branch.
- `git merge` - Aligns and merges missed changes between your local branch and a remote repository. 
- `git pull` - Gets changes from a remote repository, and merges them with the changes on your local branch.

    > 💡 **Tip:**
    Using ``` git fetch``` followed by ```git merge``` allows you to see and review the changes you are merging with your local branch before the merge happens. This is ultimately what ```git pull``` does by merging changes on to your local branch.

If any changes on your local branch are out of sync with the changes on the remote repository, a divergence can occur and result in an error. To fix this, sync your local branch with the remote master branch on the repository by using the `git merge origin/master` command. This merges any missed changes from your local branch with the repository master branch.

For more information on Git commands, features, and functions, see [Introduction to GitHub](https://github.com/skills/introduction-to-github).