## Level 12
Login into the server via ssh using the following command

```
ssh -p 2220 bandit12@bandit.labs.overthewire.org
```
Then enter the password you got in previous level  
You will be logged in

Follow these commands to access the password for the next level
```
ls #data.txt
```
We need to make some new files which we can't do in the current directory so first we create a folder ```cosign``` in ```tmp``` folder in root directory 

```
mkdir /tmp/cosign
```
Now copy this ```data.txt``` file to /tmp/cosign and change directory to /tmp/cosign 
```
cp data.txt /tmp/cosign
cd /tmp/cosign
ls #data.txt
```
Now to revert hex dump to binary we use ```xxd -r``` command as 
```
cat data.txt | xxd -r > data1
file data1
```
Now it is a gzip file so first convert it to .gz extension and decode it with ```gzip -d```
```
mv data1 data2.gz
gzip -d data2.gz
file data2
```
Now it is a bzip2 file so first convert it to .bz extension and decode it with ```bzip2 -d```
```
mv data2 data3.bz
bzip2 -d data3.bz
file data3
```
Now it is a gzip file again so first convert it to .gz extension and decode it with ```gzip -d```
```
mv data3 data4.gz
gzip -d data4.gz
file data4
```
Now it is a tar file so first convert it to .tr extension and decode it with ```tar -xf```
```
mv data4 data5.tr
tar -xf data5.tr
ls # data5.bin
file data5.bin

```
Again a tar file ,Do same 
```
mv data5.bin data6.tr
tar -xf data6.tr
ls # data6.bin
file data6.bin
```
Umm, it's a bzip file now ,So..
```
mv data6.bin data7.bz
bzip2 -d data7.bz
file data7
```
And it's a tar file 
```
mv data7 data8.tr
tar -xf data8.tr
ls #data8.bin
file data8.bin
```
gzip file again 
```
mv data8.bin data9.gz
gzip -d data9.gz
file data9
```
Finally its a ASCII Text which one can cat 
```
cat data9
```

Copy the password for level 13 and logout using exit command 
