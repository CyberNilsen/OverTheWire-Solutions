Goal:

```
The password for the next level is stored somewhere on the server and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
```

when having tried the find command we realize that wont work since there isnt a specific file or we dont know that but we can still try running the find command regardless

```
find . -type f -user bandit7 -group bandit6 -size 33c
```

this gives us nothing, 

unsure whaat to do further i tried this command instead:

```
find / -type f -group bandit6 -user bandit7 -size 33c
```

basically search for all files in the whole system, doing this gives us something but it gives us a whole lotta clutter, many files with many errors,

errors.png

therefore i need to find out how to supress/ignore the errors and still search and find out i have to add this to the command i ran above:

```
2>/dev/null
```

this results in us finding out where the password is saved.

password.png

then we can proceed to cat it.

bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj