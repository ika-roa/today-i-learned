# Change upstream URL for git repo
1. Open Git Bash.
2. Change the current working directory to your local project.
3. List your existing remotes in order to get the name of the remote you want to change.
    ```shell
    $ git remote -v
    > origin  git@github.com:OWNER/REPOSITORY.git (fetch)
    > origin  git@github.com:OWNER/REPOSITORY.git (push)
    ```
4. Change your remote's URL from SSH to HTTPS with the `git remote set-url` command.
    ```shell
    git remote set-url origin https://github.com/NEW_OWNER/NEW_REPOSITORY.git
    ```
5. Verify that the remote URL has changed.
    ```shell
    $ git remote -v
    > origin  git@github.com:NEW_OWNER/NEW_REPOSITORY.git (fetch)
    > origin  git@github.com:NEW_OWNER/NEW_REPOSITORY.git (push)
    ```
The next time you `git fetch`, `git pull`, or `git push` to the remote repository, you'll be asked for your username and password.