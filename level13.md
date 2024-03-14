## Level 13
Login into the server via ssh using the following command

```
ssh -p 2220 bandit13@bandit.labs.overthewire.org
```
Then enter the password you got in previous level  
You will be logged in

Follow these commands to access the password for the next level
```
ls # sshkey.private 
```
You get a ssh private key use this key to login to bandit14 using this command 
```
ssh -i sshkey.private bandit14@localhost -p 2220
```
Enter yes for the authentication
Now the password for the current (logged In, bandit14 ) challenge is in the etc/bandit_pass folder
```
cat /etc/bandit_pass/bandit14
``` 
Copy the password for level 14 and logout from bandit14 using exit command and then from bandit13 using exit
