# Undo initial commit in git


If you realize that there was a mistake in the initial commit and

1. You have not yet pushed 
2. You have only one commit on your `main` branch
3. There is no branch called `old_main` so you're free to use that name

Then rename the existing branch to `old_main` and create a new, orphaned, branch `main` _(like it is created for new repositories)_. Then the `old_main` can be deleted.

```
git branch -m main old_main
git checkout --orphan main
git branch -D old_main
```

Note: Moving or copying a git branch preserves its reflog while deleting and then creating a new branch destroys it. Since you want to get back to the original state with no history you probably want to delete the branch.

https://stackoverflow.com/questions/6632191/how-to-revert-initial-git-commit