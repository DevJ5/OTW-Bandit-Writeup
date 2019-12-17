__Bandit Level 7__
---
> The password for the next level is stored somewhere on the server and has all of the following properties:

> - owned by user bandit7
> - owned by group bandit6
>- 33 bytes in size

Somewhere on the server means from root, output all the non permissions to dev null.

``` bash
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
```