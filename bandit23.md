__ Bandit Level 23 __
---

> A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

`ls -lah /etc/cron.d` shows couple of cronjobs.
`cat cronjob_bandit23` shows that every minute `/usr/bin/cronjob_bandit23.sh` is being ran.

`cat /usr/bin/cronjob_bandit23.sh` shows that the md5 hash of "I am user bandit23" is the name of the file in /tmp that has the password to the next level. This file also has x permissions for group22. So I can just run the file and see the whole path.

