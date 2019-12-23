__Bandit Level 16__
---
> The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

SSL okay, the predecessor of TLS. We can use openssl for this and use it's client.

```bash
openssl s_client -connect localhost:30001
```