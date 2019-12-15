__Bandit Level 6__
---
> The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
> - human-readable
> - 1033 bytes in size
> - not executable

Let's use the find command to find a 1033 byte size file.
``` bash
#!/bin/bash
cd ~/inhere
cat $(find . -type f -size 1033c)
```