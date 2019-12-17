__Bandit Level 5__
---
> The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

Human readable means ASCII text. So lets try:
```
bandit4@bandit:~/inhere$ file ./* | grep -i asc
```

File07 seems to be ASCII.
```
#!/bin/bash
cat $(file ./* | grep -i asc | cut -d ":" -f 1)
```

