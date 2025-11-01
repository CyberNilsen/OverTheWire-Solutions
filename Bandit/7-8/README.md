Goal:

```
The password for the next level is stored in the file data.txt next to the word millionth
```

here we can use grep to find the file. But first we cant just use grep as a standalone command which i forgot and tried.... we have to use cat to read the file contents and then grep the word "millionth" to find the password since the password is next to the word as the goal stated. 

bandit7@bandit:~$ cat data.txt | grep "millionth"
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
bandit7@bandit:~$

doing what i wrote above resulted in us gaining the correct password.
