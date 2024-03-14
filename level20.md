## Level 20
Login into the server via ssh using the following command

```
ssh -p 2220 bandit20@bandit.labs.overthewire.org
```
Then enter the password you got in previous level  
You will be logged in

Follow these commands to access the password for the next level
```
ls #sucoonect
./suconnect 
```
It needs a port number 
```
echo "VxCazJaVykI6W36BkBU0mJTCM8rR95XT" | nc -l localhost 8888 &
```
The & at last opend a connection in the background at port 8888 , Now we can connect 
```./suconnect 8888```

Copy the password for level 21 and logout using exit command 
