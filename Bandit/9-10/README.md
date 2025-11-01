Goal:

```
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.
```

if we run the command strings we find the human readable strings and we can also see the password listed there aka we need to run this command:

```
strings data.txt
```

password.png

to find the password without having to guess it here, we run this command

```
strings data.txt | grep "password"
```

then we can see the password/or rather how many ===== signs there are and afterwards we run the grep command to find the real password.

```
strings data.txt | grep "=========="
```

realpassword.png

output:

```
bandit9@bandit:~$ strings data.txt | grep "=========="
========== the
========== password
E========== is
5========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
bandit9@bandit:~$
```