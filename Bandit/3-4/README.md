Reading the goal first again

```
The password for the next level is stored in a hidden file in the inhere directory.
```

and i know that to find hidden files i have to ls -a, 

inhere.png 

here we can see that we have to use ls -a and we cant use ls to find the files which makes sense.

hiddenfile.png

here we see the hidden file after running ls -a, and then i cat the file and get the password

bandit3@bandit:~/inhere$ cat ...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
bandit3@bandit:~/inhere$
