<img width="345" height="152" alt="image" src="https://github.com/user-attachments/assets/5c52d732-e0ac-4819-8057-f4d59f608d34" /># OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

# Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

# Step 2:

Execute the following commands

# Step 3:

Testing the commands for the desired output. 

# COMMANDS:
# Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
# Display the content of the files

cat < file1
### OUTPUT

<img width="318" height="155" alt="image" src="https://github.com/user-attachments/assets/ac1d4ba4-b6cb-43a7-828e-07e5ac3fab35" />


cat < file2
### OUTPUT

<img width="335" height="172" alt="image" src="https://github.com/user-attachments/assets/5f5f3d30-6b29-4886-ad57-188c1378a9da" />


# Comparing Files

cmp file1 file2
### OUTPUT

 <img width="368" height="68" alt="image" src="https://github.com/user-attachments/assets/f3ae9768-dec5-4e28-947e-3fcfb7aed379" />


  comm file1 file2
 ### OUTPUT

<img width="315" height="200" alt="image" src="https://github.com/user-attachments/assets/bba2d2b3-6234-44b9-9888-f6a2dfd55fe1" />



 diff file1 file2
### OUTPUT

<img width="312" height="269" alt="image" src="https://github.com/user-attachments/assets/c07f5e2e-b1bd-4db6-9a31-4627b17f00bb" />




# Create the following files file11, file22 as follows:

 cat > file11
```
Hello world
This is my world
^d
```
 cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


 cut -c1-3 file11
### OUTPUT

<img width="373" height="78" alt="image" src="https://github.com/user-attachments/assets/e19583d4-9a66-4433-a7d8-8765ba1b7d4e" />



 cut -d "|" -f 1 file22
### OUTPUT

<img width="479" height="97" alt="image" src="https://github.com/user-attachments/assets/6861e7e3-6930-4143-867b-05c605da5b24" />



 cut -d "|" -f 2 file22
### OUTPUT

<img width="348" height="97" alt="image" src="https://github.com/user-attachments/assets/191e3ae7-ac14-40e3-beac-c931ad881d97" />



 cat < newfile 
```
Hello world
hello world
^d
````
 cat > newfile 
<img width="349" height="185" alt="image" src="https://github.com/user-attachments/assets/5e1d1870-4820-4482-a8c1-38770c6674ec" />


 grep Hello newfile 
### OUTPUT

<img width="339" height="79" alt="image" src="https://github.com/user-attachments/assets/caa7afec-e904-4ebc-a731-71794f89c497" />



 grep hello newfile 
### OUTPUT

<img width="326" height="50" alt="image" src="https://github.com/user-attachments/assets/9e9199cb-7af8-4ec9-af14-9bcf4c4f1a29" />




 grep -v hello newfile 
### OUTPUT

<img width="336" height="86" alt="image" src="https://github.com/user-attachments/assets/b6f9e503-eed0-4910-98cd-7cc5ad1f465b" />



 cat newfile | grep -i "hello"
### OUTPUT

<img width="380" height="78" alt="image" src="https://github.com/user-attachments/assets/4c33aaaf-5f77-40b9-b6e9-4aa9fe8b52f2" />


 cat newfile | grep -i -c "hello"
### OUTPUT

<img width="412" height="83" alt="image" src="https://github.com/user-attachments/assets/e757a279-7d62-437a-bafb-390de4c5b881" />



 grep -R ubuntu /etc
### OUTPUT

<img width="935" height="808" alt="image" src="https://github.com/user-attachments/assets/ef3c0e29-e869-4fbf-81fb-58c936f07b97" />
<img width="937" height="803" alt="image" src="https://github.com/user-attachments/assets/6085a580-448a-4965-9d81-2b3fff02ae31" />
<img width="944" height="849" alt="image" src="https://github.com/user-attachments/assets/5574a8f6-4542-4a08-a4b2-663b7fed80ce" />
<img width="946" height="821" alt="image" src="https://github.com/user-attachments/assets/bf3d7b20-2aa5-48e0-8f6f-d5f40a4ffe91" />
<img width="938" height="852" alt="image" src="https://github.com/user-attachments/assets/f480f374-f79c-4484-9612-c37adaaf5ada" />
<img width="935" height="854" alt="image" src="https://github.com/user-attachments/assets/f1051f44-b171-4adf-9be7-b03f484607e3" />



 grep -w -n world newfile   
### OUTPUT

<img width="365" height="79" alt="image" src="https://github.com/user-attachments/assets/be0d65d9-5881-442e-bf52-3124c01d7b66" />



 cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

 cat > newfile

<img width="321" height="174" alt="image" src="https://github.com/user-attachments/assets/4c4e4598-9ec3-4c3a-b2e3-f16fe538c6ca" />



 egrep -w 'Hello|hello' newfile 
### OUTPUT

<img width="355" height="99" alt="image" src="https://github.com/user-attachments/assets/196f8194-f1b0-4b62-b3f4-b7c6de2dcbe4" />



 egrep -w '(H|h)ello' newfile 
### OUTPUT

<img width="366" height="100" alt="image" src="https://github.com/user-attachments/assets/9e7e0f74-1e9f-4af1-b8c7-7be5b3782ccb" />



 egrep -w '(H|h)ell[a-z]' newfile 
### OUTPUT

<img width="416" height="102" alt="image" src="https://github.com/user-attachments/assets/aee1f1e1-f44f-452a-8a9a-cca5420f1d2e" />



 egrep '(^hello)' newfile 
### OUTPUT

<img width="338" height="76" alt="image" src="https://github.com/user-attachments/assets/2f0a1fd6-4d9b-4f9f-a665-c083082a334f" />


 egrep '(world$)' newfile 
### OUTPUT

<img width="302" height="104" alt="image" src="https://github.com/user-attachments/assets/2b618462-ce0d-4f2c-bd23-0c50cbf40c44" />



 egrep '(World$)' newfile 
### OUTPUT

<img width="319" height="81" alt="image" src="https://github.com/user-attachments/assets/13dbd885-e2a7-4e97-a886-9430e6629eab" />



 egrep '((W|w)orld$)' newfile 
### OUTPUT

<img width="344" height="128" alt="image" src="https://github.com/user-attachments/assets/2c25fe34-1a9f-4bdf-94d3-0e3bb29038d3" />


 egrep '[1-9]' newfile 
### OUTPUT

<img width="355" height="82" alt="image" src="https://github.com/user-attachments/assets/ad9deb37-db5e-48fb-b3c5-d01ad23a55bc" />



 egrep 'Linux.*world' newfile 
### OUTPUT

<img width="365" height="77" alt="image" src="https://github.com/user-attachments/assets/4d04536e-8dda-4178-98e2-9cb7a52b6978" />




 egrep 'Linux.*World' newfile 
### OUTPUT

<img width="375" height="82" alt="image" src="https://github.com/user-attachments/assets/179e9fcf-2bfc-4335-bd08-a8be1e719f39" />




 egrep l{2} newfile
### OUTPUT


<img width="308" height="104" alt="image" src="https://github.com/user-attachments/assets/4b5e976f-e200-44da-a29a-d4c17f3ada53" />

 egrep 's{1,2}' newfile
### OUTPUT 

<img width="332" height="132" alt="image" src="https://github.com/user-attachments/assets/d73e9a08-d78d-4c1e-882c-0884879e87bd" />


 cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


 sed -n -e '3p' file23
### OUTPUT

<img width="322" height="80" alt="image" src="https://github.com/user-attachments/assets/cc4f8869-3ec4-4d52-be21-211436ade56d" />



 sed -n -e '$p' file23
### OUTPUT

<img width="353" height="77" alt="image" src="https://github.com/user-attachments/assets/41da88e4-096a-48b8-953b-081d6325ec74" />


sed -e '2s/Ram/Sita/' file23

### OUTPUT

<img width="359" height="253" alt="image" src="https://github.com/user-attachments/assets/57a7cfe1-f6fa-4f49-b152-74d0b1701520" />



 sed  -e '2s/Ram/Sita/' file23
### OUTPUT

<img width="382" height="253" alt="image" src="https://github.com/user-attachments/assets/ade64a82-3c06-4ef6-8248-9b4c4ac4c76f" />



 sed  '/tom/s/5000/6000/' file23
### OUTPUT

<img width="383" height="259" alt="image" src="https://github.com/user-attachments/assets/de132ad8-bc24-45d5-b8b6-c6166254c205" />



 sed -n -e '1,5p' file23
### OUTPUT


<img width="349" height="180" alt="image" src="https://github.com/user-attachments/assets/39d0153a-06b5-47bd-8319-7f00328f37ea" />


 sed -n -e '2,/Joe/p' file23
### OUTPUT

<img width="361" height="129" alt="image" src="https://github.com/user-attachments/assets/4230cd61-24ca-4d3e-a1c7-b1e1041e13ea" />


sed -n -e '/tom/,/Joe/p' file23
### OUTPUT

<img width="381" height="108" alt="image" src="https://github.com/user-attachments/assets/e019f397-880a-42e0-98dd-a367e841c704" />


 seq 10 | sed -n '4,6p'
### OUTPUT

<img width="303" height="133" alt="image" src="https://github.com/user-attachments/assets/222ce3e9-c4ef-4e4c-ab0b-37cc5dcf9079" />


 seq 10 | sed -n '2,~4p'
### OUTPUT

<img width="312" height="136" alt="image" src="https://github.com/user-attachments/assets/4a82b5a6-7a34-4121-9f6a-7c6cab33d352" />

 seq 3 | sed '2a hello'
### OUTPUT


<img width="345" height="152" alt="image" src="https://github.com/user-attachments/assets/f7740098-b055-4d6c-99de-d3e9a34fcb18" />

seq 2 | sed '2i hello'

### OUTPUT

<img width="357" height="126" alt="image" src="https://github.com/user-attachments/assets/fb295033-b58f-4a49-b80b-35b65314dde3" />


 seq 10 | sed '2,9c hello'
### OUTPUT

<img width="351" height="124" alt="image" src="https://github.com/user-attachments/assets/e4805d46-9391-4e1a-adba-066461463658" />


 sed -n '2,4{s/^/$/;p}' file23
### OUTPUT

<img width="441" height="127" alt="image" src="https://github.com/user-attachments/assets/c69601f4-03ca-4435-8f09-f926d05f265e" />

 sed -n '2,4{s/$/*/;p}' file23
### OUTPUT

<img width="444" height="129" alt="image" src="https://github.com/user-attachments/assets/3a4f4f21-0bd2-4479-8b31-d9d778251f26" />

#Sorting File content
 cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
 sort file21
### OUTPUT
<img width="332" height="178" alt="image" src="https://github.com/user-attachments/assets/bd0b0515-1b6f-4b30-a4d5-6c01726d74e9" />



 cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
 uniq file22
### OUTPUT

<img width="317" height="178" alt="image" src="https://github.com/user-attachments/assets/e9c86f1f-a506-486e-bcc5-16829765d4c0" />



#Using tr command

 cat file23 | tr [:lower:] [:upper:]
 ### OUTPUT

<img width="425" height="241" alt="image" src="https://github.com/user-attachments/assets/6e7f36c2-c617-4942-a834-e40c775bcb88" />


 cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
 cat < urllist.txt

<img width="384" height="125" alt="image" src="https://github.com/user-attachments/assets/5fc889ad-6d99-42b6-aa48-28f9cd576a2c" />

cat > urllist.txt
'''
www. yahoo. com
www. google. com
www. mrcet.... com
'''
cat urllist.txt | tr -d ' '

### OUTPUT

<img width="318" height="150" alt="image" src="https://github.com/user-attachments/assets/f070380e-816a-4902-990d-48112d5619d3" />

 
 cat urllist.txt | tr -d ' ' | tr -s '.'
### OUTPUT

<img width="503" height="130" alt="image" src="https://github.com/user-attachments/assets/188ec64c-980e-47b7-88df-3e80bdc9fd05" />


#Backup commands
 tar -cvf backup.tar *
### OUTPUT

<img width="320" height="296" alt="image" src="https://github.com/user-attachments/assets/e04154e2-44c3-4c13-a0cb-c55e10b15960" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
### OUTPUT


<img width="638" height="432" alt="image" src="https://github.com/user-attachments/assets/4e15ab2e-30b8-427e-b690-f22d96dc2c11" />


tar -xvf backup.tar
### OUTPUT

<img width="351" height="274" alt="image" src="https://github.com/user-attachments/assets/6c5a8233-7dbb-4c84-a684-c9316f79ca42" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
### OUTPUT

<img width="367" height="140" alt="image" src="https://github.com/user-attachments/assets/54ee28bd-9b61-439f-bd18-f4617eff83d2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
### OUTPUT



cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$

ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

### OUTPUT

 <img width="264" height="70" alt="image" src="https://github.com/user-attachments/assets/3fb3b506-9290-45c2-ac90-d106bd685ebb" />

ls file1
### OUTPUT

<img width="258" height="92" alt="image" src="https://github.com/user-attachments/assets/fa370977-a6a5-4e81-91b6-e7e4e1203724" />


echo $?
### OUTPUT 

<img width="323" height="93" alt="image" src="https://github.com/user-attachments/assets/3779e140-8c05-4957-9602-0ab3ee588bef" />

 
# mis-using string comparisons

cat > strcomp.sh 
```bash
#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
### OUTPUT

<img width="425" height="290" alt="image" src="https://github.com/user-attachments/assets/bdf97815-4cdb-46a9-939f-b3b2616a48ab" />


chmod 755 strcomp.sh
 
./strcomp.sh 
### OUTPUT

<img width="393" height="101" alt="image" src="https://github.com/user-attachments/assets/870c31d3-7dfc-4ec1-b51a-93650b939c1d" />


# check file ownership
cat > psswdperm.sh 
```bash
#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
### OUTPUT

<img width="637" height="175" alt="image" src="https://github.com/user-attachments/assets/015ff9de-cc7d-43e9-80f6-ca7edcce51d7" />

# check if with file location
cat>ifnested.sh 
```bash
#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
### OUTPUT

<img width="566" height="236" alt="image" src="https://github.com/user-attachments/assets/a36e522e-ea41-4da2-a2c1-b6d2f5881c2e" />



# using numeric test comparisons
cat > iftest.sh 
```bash
#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT




# check if a file
cat > ifnested.sh 
```bash
#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT




# looking for a possible value using elif
cat > elifcheck.sh 
```bash
#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
### OUTPUT



# testing compound comparisons
cat> ifcompound.sh 
```bash
#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
### OUTPUT



# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
$ ./casecheck.sh 
### OUTPUT



cat > whiletest
```bacd
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh

### OUTPUT



 
cat > untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
$ ./untiltest.sh

### OUTPUT

 

cat > forin1.sh 
```bash
#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
$ ./forin1.sh

### OUTPUT

 

cat > forin2.sh 
```bash
#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat > forin2.sh 
```bash
#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 

# OUPUT

 

cat > forin3.sh 
```bash
#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 

 ### OUTPUT



cat > forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh
$ ./forin1.sh

### OUTPUT



cat > forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file"
done
```
$ chmod 777 forinfile.sh
$ cat > cities
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```
### OUTPUT




cat > forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 

### OUTPUT



cat > forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 

### OUTPUT



cat > fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```

$ chmod 755 fornested1.sh

$ ./fornested1.sh 

### OUTPUT



 
cat > forbreak.sh 
```bash
#!/bin/bash
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed"
```

$ chmod 755 forbreak.sh
$ ./forbreak.sh 

### OUTPUT



 
cat > forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed"
```

 
$ chmod 755 forcontinue.sh

$ ./forcontinue.sh 

### OUTPUT



cat > exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 

### OUTPUT




 cat > exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. "
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
### OUTPUT


 
cat > funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```

$ chmod 755 funcex.sh
$ ./funcex.sh 
$ ./funcex.sh 1 2
### OUTPUT

 
cat > argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

### OUTPUT

 

 cat > argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

### OUTPUT



cat > argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```

$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
### OUTPUT
 
 

cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
### OUTPUT 



cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
$ chmod 777 palindrome.sh
$ ./palindrome.sh

### OUTPUT 




# RESULT:
The Commands are executed successfully.
