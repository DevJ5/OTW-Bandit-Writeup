__ Bandit Level 32 __
---

> There is a git repository at ssh://bandit31-git@localhost/home/bandit31-git/repo. The password for the user bandit31-git is the same as for the user bandit31.

The readme reveals pushing a key.txt remotely.

Let's create this file
`echo "May I come in?" > key.txt`
`git add .`
Nothing was added. *.txt is a apparntly a wildcard in gitignore. Ill clean that.

`git status` seems we have our modified file now.
`git commit -m "please" && git push origin master`

