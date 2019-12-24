__ Bandit Level 17 __
---
> The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

Do an nmap scan `nmap -sC localhost -p31000-32000` shows
PORT      STATE    SERVICE
31518/tcp filtered unknown
31790/tcp open     unknown

`nmap -sV -A -p 31000-32000 localhost | grep open` shows
31790/tcp open     ssl/unknown
```
openssl s_client -connect localhost:31790 -quiet < /etc/bandit_pass/bandit16 > /tmp/pkeyto17.txt

chmod 600 /tmp/pkeyto17.txt
ssh -i /tmp/pkeyto17.txt bandit17@localhost
```
