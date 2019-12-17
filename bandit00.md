__Bandit Level 0__
---
[Go to overthewire.org](https://overthewire.org/wargames/bandit/bandit0.html)
> The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

Property      | Value
---           | ---
Host          | bandit.labs.overthewire.org
Port          | 2220
Username      | bandit0
Password      | bandit0

Downloaded and tested putty, an open source ssh and telnet client for windows. Telnet has no authentication and is not encrypted.

Will use ssh for the remainder of this CTF. SSH uses public key cryptograhy, also known as assymetric cryptography.
SSH provides a secure channel over an unsecured network in a client–server architecture, connecting an SSH client application with an SSH server.

SSH can transfer files with SFTP and SCP. Standard port is 22.

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```



