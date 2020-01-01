__ Bandit Level 30 __
---

> There is a git repository at ssh://bandit29-git@localhost/home/bandit29-git/repo. The password for the user bandit29-git is the same as for the user bandit29.

Clone the repository and find the password for the next level.

Same as before we cloned the repository. Checked out the first commit, but nothing. It says something about production, so are there other branches?

`git branch -a` shows a dev and sploits-dev.
`git checkout dev` is the correct one.

