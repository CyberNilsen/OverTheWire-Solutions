Goal:

```
The password for the next level is stored in the file data.txt, which contains base64 encoded data
```

here we can run cat data.txt and grep "==" 

since we know that base64 data thats encoded are useally/have 2 == signs in them.

```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt | grep "=="
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
bandit10@bandit:~$
```

Here we see our potential password, then we decode it using this command:

```
bandit10@bandit:~$ cat data.txt | grep "==" | base64 -d
```

and we also find the correct password.

```
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
bandit10@bandit:~$
```