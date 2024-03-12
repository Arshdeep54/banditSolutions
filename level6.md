## Level 6
Login into the server via ssh using the following command

```
ssh -p 2220 bandit6@bandit.labs.overthewire.org
```
Then enter the password you got in previous level  
You will be logged in

Follow these commands to access the password for the next level
```
 find -size 33c -user bandit7 -group bandit6
```
 Find the file which do not have permision denied written 
 ``` cat {file name}```


Copy the password for level 7 and logout using exit command 
