## Level 16
Login into the server via ssh using the following command

```
ssh -p 2220 bandit16@bandit.labs.overthewire.org
```
Then enter the password you got in previous level  
You will be logged in

First Find Out which port is available using ```nmap```
```
 nmap -A -T4 localhost -p 31000-32000 
```
It might take some time .
Now connect to the ss/unknow port using 
```
 openssl s_client localhost:31790
```
And type the password here 
You will get a ssh private key .
now we want to create a private key file which we can not in current directory 
```
cd /tmp
mkdri banditssh
cd banditssh
nano sshkey.private
```
Enter the key and save . Also give read only permision before connecting 
```
chmod 400 sshkey.private
```
Connect and you will login as bandit17 user who can access the password in etc/bandit_pass folder
```
ssh -i ssh.private bandit17@localhost -p 2220
cat /etc/bandit_pass/banit17
```

Copy the password for level 17 and logout using exit command 
