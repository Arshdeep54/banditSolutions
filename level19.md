## Level 19
Login into the server via ssh using the following command

```
ssh -p 2220 bandit19@bandit.labs.overthewire.org
```
Then enter the password you got in previous level  
You will be logged in

Follow these commands to access the password for the next level
```
ls #bandit20-do
file bandit20-do
```
This is a executable file 
```./bandit-20``` : It needs an id 

```
 ./bandit20-do cat /etc/bandit_pass/bandit20
```

Copy the password for level 20 and logout using exit command 
