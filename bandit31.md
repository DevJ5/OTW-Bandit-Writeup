__ Bandit Level 31 __
---

> There is a git repository at ssh://bandit30-git@localhost/home/bandit30-git/repo. The password for the user bandit30-git is the same as for the user bandit30.

Clone the repository and find the password for the next level.

This repo has only a master branch and 1 commit. I went through all the files in the .git repository and stumbled upon packed-refs. It shows refs/tags/secret and a hash.

There might a version that is tagged. `git tag` shows secret. `git show secret` shows us the password.