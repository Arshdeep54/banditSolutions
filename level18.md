## Level 18
Login into the server via ssh using the following command

```
ssh -p 2220 bandit18@bandit.labs.overthewire.org
```
Then enter the password you got in previous level  
You will be logged in
Ya Byebye

So now We somehow need to take out the data i.e readme file from the server to our local machine 
```
 scp -P 2220 bandit18@bandit.labs.overthewire.org:readme .
```
the last ```.``` means to mv it to current directory 
Now simply ```cat readme``` to get the password 

Copy the password for level 19 and logout using exit command 
