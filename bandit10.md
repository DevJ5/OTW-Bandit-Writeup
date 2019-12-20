__Bandit Level 10__
---
> The password for the next level is stored in the file data.txt in one of the few human-readable strings, beginning with several ‘=’ characters.

`cat data.txt` Gibberish binary with some text in it. Use `strings`on it with a `grep -P "^=+"`. Probably all these flags are md5 hashes which have 32 hexadecimal characters (16 bytes / 128 bits).

