Bandit Level 14
---
> The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on.

We find a private key. We can use ssh with this file as a private key to login to localhost.

``` bash
-i sshkey.private bandit14@localhost
```