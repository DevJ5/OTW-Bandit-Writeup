__ Bandit Level 22 __
---

> A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

`cd /etc/cron.d ls` shows a couple of jobs.
`cat cronjob_bandit22` shows there is .sh script being run every minute from /usr/bin/cronjob_bandit22.sh and the stdout and stderr are both being redirected to /dev/null.

`cat /usr/bin/cronjob_bandit22.sh` shows the password is being catted to /tmp/

And we can cat this out ourselves.
