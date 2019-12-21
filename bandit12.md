__Bandit Level 12__
---
> The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

Some sort of caesar cipher, we can install rot13 for that.

``` bash
#!bin/bash
echo "Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh" | rot13 | awk '{print $4}'
```