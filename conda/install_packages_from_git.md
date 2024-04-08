# Install packages from git repo
## Install packages
pip supports installing packages from various version control systems (VCS), for example `git`. Specify username, repo, and, after the @ symbol, the branch and an egg name that pip uses for the installation:

`pip install git+ssh://git@gitlab/mak/helixscreener.git@main#egg=helixscreener`

## Editable mode and updates
With the prefix `-e` or `--editable` the package can be installed in editable mode, and easily changed after an update to the remote repo with

`pip install -I -e git+ssh://git@gitlab/mak/helixscreener.git@main#egg=helixscreener`