__Bandit Level 9__
---
> The password for the next level is stored in the file data.txt and is the only line of text that occurs only once.

A `cat data.txt | less` shows lines with what appear to be hashes. Uniq only sorts when lines are adjacent, use count options to get the count on how many times they occur, pipe through regex and cut the flag.

``` bash
#!/bin/bash
sort data.txt | uniq -c | grep -P "^\s+1[^0-9]" | awk '{print $2}'
```

Awk also has builtin regex, but \s doesnt work as whitespace. Apparantly this is because \s is a GNU Awk thing. Putting an actual space does seem to do the trick.

`sort data.txt | uniq -c | awk '/^ *1[^0-9]/ {print}'`