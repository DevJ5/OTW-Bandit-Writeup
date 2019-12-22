__Bandit Level 13__
---
> The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

To reverse a hexdump `xxd -r data.txt newfile.txt`. `cat newfile.txt`. Seems like it's still gibberish. `file newfile.txt` shows that it is a gzip compressed file. `mv newfile.txt newfile.gz`. `gunzip newfile.gz`. Then `file` show bunzip2 data. `bunzip2`. This cycle continues for a while mixed with some POSIX tar archives, which use `tar -xvf`.