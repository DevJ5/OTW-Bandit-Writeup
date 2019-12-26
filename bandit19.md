__Bandit Level 19__
---

> The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

Let's see if I can copy my public key on the machine.

`ssh-copy-id bandit18@bandit.labs.overthewire.org -p 2220` returns cannot create directory .ssh.

Let's see if I can ls the home directory remotely.
`ssh bandit18@bandit.labs.overthewire.org -p 2220 "ls ~ -lah" > ~/Desktop/lshome.txt`

total 24K
drwxr-xr-x  2 root     root     4.0K Oct 16  2018 .
drwxr-xr-x 41 root     root     4.0K Oct 16  2018 ..
-rw-r--r--  1 root     root      220 May 15  2017 .bash_logout
-rw-r-----  1 bandit19 bandit18 3.5K Oct 16  2018 .bashrc
-rw-r--r--  1 root     root      675 May 15  2017 .profile
-rw-r-----  1 bandit19 bandit18   33 Oct 16  2018 readme

I only have read permissions with the password from 18. So I cant change the bashrc, but I could just cat the readme file and output it locally or copy it over completely with scp.

```bash
#!/bin/bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat readme" > ~/Desktop/cat_readme.txt
```

