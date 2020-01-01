__ Bandit Level 26 __
---

> Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

Lets check what shell it uses:
`cat /etc/passwd | grep bandit26` shows /usr/bin/showtext as a shell...
`cat /usr/bin/showtext`

It opens ~/text.txt in more. Now we can screw with more by adjusting the terminal size so it stays in the buffer. From this buffer we can execute commands with !. `! /bin/sh` doesnt work. `!bash` doesnt work. 

Hmm that doesn't seem to work here. We can also enter vim with `v`.

Enter a shell from vim `:!/bin/sh` Doesn't work either...

`:set shell=/bin/bash`
`:shell`
Finally gives us a shell.


We can also read from files using `:r /etc/bandit_pass/bandit26` in VIM.