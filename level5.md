## Level 5
Login into the server via ssh using the following command

```
ssh -p 2220 bandit5@bandit.labs.overthewire.org
```
Then enter the password you got in previous level  
You will be logged in

Follow these commands to access the password for the next level
```
find -size 1033c ! -executable # file size check and non-executable
```
You get a file ./inhere/maybehere07/.file2  
To check if this is human readable ``` file ./inhere/maybehere07/.file2```  
It will say its an ascii text   
So all three conditions verified  


Copy the password for level 6 and logout using exit command 
