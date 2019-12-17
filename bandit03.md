__Bandit Level 3__
---
> The password for the next level is stored in a file called spaces in this filename located in the home directory

`ls` results in a filename with spaces in it. I know tab autocompletion works on this, but I could also escape all the spaces with backslashes, like so `cat spaces\ in\ this\ filename`

```
bandit2@bandit:~$ cat spaces\ in\ this\ filename
```