Goal:

```
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable
```

from the last level we know we have to do the same but use multiple arguments

ls.png

here we can see that there are lots of directories, and inside one of those directories there are lots of files

```
bandit5@bandit:~/inhere/maybehere00$ ls
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3
bandit5@bandit:~/inhere/maybehere00$
```

as we can see....

to find the correct file we run this command: 

```
find . -type f ! -executable -size 1033c -readable
```

. is to search in the current directory -type f is to search for files/file the ! is to say not and then we combine that with executable meaning search for files that are not executable, then we search for the size/bytes then we command a argument in the find command all we have to do here is -size 1033c and then for the readable part we do -readable, then run that command and we find the correct file, then we can cat that file to open it.

find.png

here we can see the content and what we did worked.

```
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```