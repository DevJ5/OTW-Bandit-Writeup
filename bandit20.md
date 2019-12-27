__ Bandit Level 20 __
---

> To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

`ls -l ` lists us a file whet the SUID set. Meaning we can run this file as the owner of the file which is bandit20.

`file` shows us it's a 32-bit executable.

`./bandit20-do` shows how to run this command. We can use this program to run a command as another user.

Guess is to just `cat` out the password for bandit20 with this command.

```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```