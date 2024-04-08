# Update forked repo

Add a secondary remote called `upstream`.
```
git remote add upstream https://...
```
Fetch the remote and then pull its changes into your local default branch, for example `main`.
```
git checkout main
git fetch upstream
git pull upstream main
```
Last, push to your own remote `origin` to keep the forked repo in sync.
```
git push origin main
```
Based on the default main branch, you can continue with creating branches, e.g. `git checkout -b feature/...`.
## Important!
**Never** work on the default branch (main/master, check your project settings) of your fork, but only create change commits in feature and fix branches!

https://forum.gitlab.com/t/refreshing-a-fork/32469