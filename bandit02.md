__Bandit Level 2__
---
> The password for the next level is stored in a file called - located in the home directory

I know `cd -` switches back and forth between current and last visited directory. 

`cat -` gives me standard input. So I need to provide the full/relative path.

```
bandit1@bandit:~$ cat ./-
```

Apparantly, using `-` as a filename to mean stdin/stdout is a convention that a lot of programs use. 

You can also use `/dev/stdin` and `/dev/stdout`. 