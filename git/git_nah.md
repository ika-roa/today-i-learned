# git nah

Did you ever write something out and then felt like "nah...". Now you can put your thoughts into action with this handy alias. Reset any local and staged changes as if nothing happened.

`git config --global alias.nah "!git reset --hard && git clean -df"`

Notice the exclamation mark. It needs this so we can run custom commands. This allows us to combine two git commands.

[https://dev.to/michi/handy-git-aliases-5ag3]
