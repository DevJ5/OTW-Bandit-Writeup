__Bandit Level 15__
---
> The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

Use either telnet or netcat to connect to port 30000. Cat out the password `cat /etc/bandit_pass/bandit14`.

```bash
nc localhost 30000
```