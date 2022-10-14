# Working with branches in git

## Creating branches

1.  Every time you start working on a new feature or bugfix, you should create a new branch for this topic
2.  `git branch my-branch`
3.  `git checkout my-branch`
4.  work on branch

    -   split the feature’s implementation into logical chunks
    -   finish one step before starting with another
    -   test each step
    -   commit early and often, but do not commit half-done work!

6.  `git push -u origin my-branch`

## Merging branches

1.  code that gets integrated into `main` must be stable!
2.  `git checkout main`
3.  `git merge my-branch`

## Deleting branches

1.  `git branch -d my-branch`
2.  `git push origin --delete my-branch`