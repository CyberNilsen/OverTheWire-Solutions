Goal:

```
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
```

knowing that its a line thats unique we know do use the command uniq. We also dont need to use grep here, we have to sort the txt first and then run the command uniq -u to find the unique line. 

resulting in us finding the correct line/password

bandit8@bandit:~$ sort data.txt | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
bandit8@bandit:~$