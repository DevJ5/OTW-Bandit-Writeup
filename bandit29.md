__ Bandit Level 29 __
---
> There is a git repository at ssh://bandit28-git@localhost/home/bandit28-git/repo. The password for the user bandit28-git is the same as for the user bandit28.

Clone the repository and find the password for the next level.

The same as last level, clone the repo.

`cat README` shows credentials, but the password is all x's.

`cat /etc/passwd` shows this level is a git-shell:
bandit28-git:x:11528:11528::/home/bandit28-git:/usr/bin/git-shell

`git log` shows the hash of the initial commit. we can check this out.

`git checkout 186a1038cc54d1358d42d468cdc8e3cc28a93fcb`

Got it. `git checkout - ` to go back to last commit.