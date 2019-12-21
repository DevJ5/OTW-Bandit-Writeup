__Bandit Level 11__
---
> The password for the next level is stored in the file data.txt, which contains base64 encoded data

Decode this string using `-d` flag:

```
#!bin/bash
cat data.txt | base64 -d | awk '{print $4}'
``` 