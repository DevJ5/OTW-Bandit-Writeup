__ Bandit Level 22 __
---
 
> There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

Set up a netcat listener `nc -nlvvp 31000`
Connect to it from another terminal `./suconnect 31000`
Transmitting the password gives back another password.