# Undo git add

Git does _not automatically_ include changes in a commit: they have to be explicitly added to the next commit, with the `git add` command.

If a certain file should _not_ be part of the next commit after all, there are different options:

---
## Using git restore to Undo git add

`git restore --staged .` or `git restore --staged <individual_file>`.

This will remove the file from Git's staging area, making sure it is NOT part of the next commit.

If, at the same time, you also want to discard any local changes in this file, you can simply omit the `--staged` flag:

`git restore <individual_file>`

This will undo any modifications in this file since you last committed it. But careful with this command: _undoing uncommitted local changes cannot be undone!_

---
## Using git reset to Undo git add

The `restore` command is a quite recent addition to Git (in version 2.23). If you're using an older Git version, you have to resort to the `git reset` command to achieve the same results:

`git reset index.html`

Just like `git restore`, this will remove the file from Git's staging area and thereby NOT include it in the next commit. The local changes themselves are _not_ affected by this command.
