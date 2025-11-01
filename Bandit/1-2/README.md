First i read the goal, here i saw this

```
The password for the next level is stored in a file called - located in the home directory
```

this tells me that the file is called - therefore we have to run ls then cat the file name, when trying to cat - it does not return anything since this isnt how we are supposed to cat those type of file names, we have to run cat ./- which basically is open the file in the directory i am in and idk what else, please help me explain this copilot!!

bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat
-             .bash_logout  .bashrc       .profile
bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx

After running the command above i got the password :D