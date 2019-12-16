__Bandit Level 8__
---
> The password for the next level is stored in the file data.txt next to the word millionth

Let's do a wordcount first, `wc -lwc data.txt`. 98567 lines... 
See how it looks `tail data.txt`.

``` bash
#!/bin/bash
grep -in "millionth"  data.txt | awk '{print $2}'
```