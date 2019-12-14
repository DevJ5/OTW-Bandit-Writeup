__Bandit Level 4__
---
[Go to overthewire.org](https://overthewire.org/wargames/bandit/bandit4.html)
> The password for the next level is stored in a hidden file in the inhere directory.

Hidden means `ls -la`, this reveals the directory `inhere`.

`cd inhere`
`ls -la` reveals a file `.hidden`
`cat .hidden` for the flag.