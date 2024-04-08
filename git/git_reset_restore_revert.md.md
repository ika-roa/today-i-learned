# Reset, restore and revert

There are three commands with similar names: `git revert`, `git restore` and `git reset`.

- [[git_reset_restore_revert.md#git revert | git revert]] is about making a new commit that reverts the changes made by other commits.
- [[git_reset_restore_revert.md#git restore| git restore]] is about restoring files in the working tree from either the index or another commit. This command does not update your branch. The command can also be used to restore files in the index from another commit.
- [[git_reset_restore_revert.md#git reset|git reset]] is about updating your branch, moving the tip in order to add or remove commits from the branch. This operation changes the commit history.

## git revert
**The `git revert` command helps you undo an existing commit.**

It's important to understand that it does _not_ delete any data in this process: instead, Git will create _new_ changes with the opposite effect - and thereby undo the specified old commit.
### Important Options
#### commit-hash
**Specifies the commit you want to undo.** Note that you can also provide multiple commit hashes if you want to revert multiple commits in one go.
#### --no-commit
**Does not directly commit the created changes.** By default, the reverting changes would be directly committed by Git. With the "--no-commit" option, the changes will only be created, but not committed. You could then edit them further and commit them manually.
#### --no-edit
**Use the default commit message that Git suggests.** By default, you would be prompted to enter a commit message for the new commit that is about to be created in the process. Using "--no-edit", however, you signal that you do _not_ want to provide your own message, but simply go with the standard message that Git proposes.


## git restore
**The `git restore` command helps to unstage or even discard uncommitted local changes.**

On the one hand, the command can be used to undo the effects of `git add` and unstage changes you have previously added to the Staging Area.
On the other hand, the `restore` command can also be used to discard local changes in a file, thereby restoring its last committed state.
### Important Options
#### filename
**The name of a file (or multiple files) you want to restore.** Naming the file you want to restore can be as simple as providing the filename / path to a single file. But you can also provide multiple filenames (delimited by spaces) or even a wildcard pattern (e.g. `*.html`). Another option is to provide the `.` character, thereby restoring all files in the current directory.
#### --staged
**Removes the file from the Staging Area, but leaves its actual modifications untouched.** By default, the `git restore` command will discard any local, uncommitted changes in the corresponding files and thereby restore their last committed state. With the `--staged` option, however, the file will only be removed from the Staging Area - but its actual modifications will remain untouched.
#### --patch
**Allows you to select individual chunks to restore.** Git steps through all of the individual chunks of changes in an interactive way and asks you, for each chunk, if you want to discard/unstage it.


## git reset
**The `git reset` command does not create a new commit, but effectively goes back in time to a state in the past and calls that current.** This is really helpful if you need to take a new direction in your work and don’t mind discarding the latest commits. A reset is an operation that takes a specified commit and resets the "three trees" (working directory, staged snapshot, commit history) to match the state of the repository at that specified commit. A reset can be invoked in three different modes which correspond to the three trees.
### Important options
#### `--soft` 
The staged snapshot and working directory are not altered in any way.
#### `--mixed` 
The staged snapshot is updated to match the specified commit, but the working directory is not affected. This is the default option.
#### `--hard`
The staged snapshot and the working directory are both updated to match the specified commit.