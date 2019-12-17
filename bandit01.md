__Bandit Level 1__
---
> The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

The prompt shows we are in home directory.
```
bandit0@bandit:~$ cat readme
```
Hit `CTRL+D` (End of Transmission/End of File) or type `exit`. If a ssh session is stuck, hit `Enter ~.`

I'm installing sshpass. Using it as follows with command substitution:
```
me@vm:~$ sshpass -p $(cat bandit1) ssh bandit1@bandit.labs.overthewire.org -p 2220
```