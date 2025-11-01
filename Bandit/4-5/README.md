Goal

```
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
```

here i know i have to use the command find/file to find the only human-readable file, but i dont remember the command so i had to use google to find out, 

after researching a bit i found out the command was 

```
file ./*
```

to see all the files and what type of data/files they are.

humanreadable.png

now that we know the correct one we cat that file

bandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
bandit4@bandit:~/inhere$

trying all the files manually is possible of course but tiring and unnessary, example of file that is not human readable:

```
bandit4@bandit:~/inhere$ cat ./-file00
�6);/:ˋd�Jhp␦r��}�k'���vjbandit4@bandit:~/inhere$
```
