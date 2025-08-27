# OS-Linux-commands-Shell-scripting
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

<img width="331" height="152" alt="image" src="https://github.com/user-attachments/assets/6c3e196f-d165-408b-ba81-65642fc5e06e" />


cat < file2
### OUTPUT

<img width="382" height="181" alt="image" src="https://github.com/user-attachments/assets/cf80ee15-829a-4aaa-adb3-3f9153ca64d4" />

# Comparing Files

cmp file1 file2
### OUTPUT

<img width="407" height="85" alt="image" src="https://github.com/user-attachments/assets/3010859e-eb54-4afc-b93f-058c13c81f6b" />

  comm file1 file2
 ### OUTPUT

<img width="498" height="310" alt="image" src="https://github.com/user-attachments/assets/4110bbb8-bd17-484e-911d-7536d1cf16b2" />


 diff file1 file2
### OUTPUT

<img width="459" height="311" alt="image" src="https://github.com/user-attachments/assets/e9410780-fa56-4296-8473-810619f5a4df" />



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

<img width="388" height="107" alt="image" src="https://github.com/user-attachments/assets/1a510fa8-3eed-4830-afde-1859f7635915" />


 cut -d "|" -f 1 file22
### OUTPUT

<img width="398" height="140" alt="image" src="https://github.com/user-attachments/assets/d789a904-539b-4ac8-a2f3-b7202fb3a890" />


 cut -d "|" -f 2 file22
### OUTPUT

<img width="343" height="151" alt="image" src="https://github.com/user-attachments/assets/2786efeb-5221-47f4-b380-8460b3752442" />


 cat < newfile 
```
Hello world
hello world
^d
````
 cat > newfile 
<img width="366" height="207" alt="image" src="https://github.com/user-attachments/assets/d4a27228-58d7-4e75-a037-8cf89f0ec370" />

 grep Hello newfile 
### OUTPUT

<img width="528" height="85" alt="image" src="https://github.com/user-attachments/assets/233b2c05-cb8b-4f67-93ac-e9623436e569" />


 grep hello newfile 
### OUTPUT

<img width="329" height="109" alt="image" src="https://github.com/user-attachments/assets/3f63eb02-0952-47b4-8c59-c1373b86c7b1" />



 grep -v hello newfile 
### OUTPUT

<img width="355" height="86" alt="image" src="https://github.com/user-attachments/assets/fb5555e9-6504-4d3c-af62-ef5bb98f2c95" />


 cat newfile | grep -i "hello"
### OUTPUT

<img width="443" height="106" alt="image" src="https://github.com/user-attachments/assets/f2307a85-db32-4323-b9f9-1a4cc83a9239" />

 cat newfile | grep -i -c "hello"
### OUTPUT

<img width="456" height="96" alt="image" src="https://github.com/user-attachments/assets/ee3663a3-35dd-4d04-9f87-740783675a97" />


 grep -R ubuntu /etc
### OUTPUT

<img width="1443" height="754" alt="image" src="https://github.com/user-attachments/assets/3bccd7c7-0eea-4aed-a318-0ac38a28d2a0" />
<img width="1409" height="763" alt="image" src="https://github.com/user-attachments/assets/f929e7d7-5626-4d88-97eb-1b2652e5e0c1" />
<img width="1420" height="722" alt="image" src="https://github.com/user-attachments/assets/23794224-fe5e-4b37-a762-6c099fac22b6" />
<img width="410" height="123" alt="image" src="https://github.com/user-attachments/assets/301f4791-dae5-4fb4-bf80-4d3d1ee2bdc6" />


 grep -w -n world newfile   
### OUTPUT

<img width="1384" height="727" alt="image" src="https://github.com/user-attachments/assets/02d0ec0e-7492-46a6-b604-0e988a48e464" />


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

<img width="346" height="200" alt="image" src="https://github.com/user-attachments/assets/a627f67f-52b2-4814-9252-f242d063e403" />

 egrep -w 'Hello|hello' newfile 
### OUTPUT

<img width="420" height="111" alt="image" src="https://github.com/user-attachments/assets/6cf4c583-a149-493f-864f-47c18139f85d" />


 egrep -w '(H|h)ello' newfile 
### OUTPUT

<img width="408" height="96" alt="image" src="https://github.com/user-attachments/assets/dbc014b3-0657-4faa-94de-98c46d8e47c8" />


 egrep -w '(H|h)ell[a-z]' newfile 
### OUTPUT

<img width="425" height="110" alt="image" src="https://github.com/user-attachments/assets/0e4ee143-2a62-42a8-97ae-ce8f1ab5f98b" />



 egrep '(^hello)' newfile 
### OUTPUT

<img width="390" height="89" alt="image" src="https://github.com/user-attachments/assets/ffc892ce-df31-4560-a7a9-c085fa54c2eb" />


 egrep '(world$)' newfile 
### OUTPUT

<img width="395" height="137" alt="image" src="https://github.com/user-attachments/assets/b3b5f5e2-1f93-4074-b809-428a843a96fe" />


 egrep '(World$)' newfile 
### OUTPUT

<img width="397" height="88" alt="image" src="https://github.com/user-attachments/assets/95f7df9c-b62b-4abc-b485-a3f01f55149b" />


 egrep '((W|w)orld$)' newfile 
### OUTPUT

<img width="439" height="139" alt="image" src="https://github.com/user-attachments/assets/2690a2fe-834d-46bd-83dc-f31181ae8ef3" />


 egrep '[1-9]' newfile 
### OUTPUT

<img width="407" height="90" alt="image" src="https://github.com/user-attachments/assets/12eefc6b-8688-40aa-8d04-fdbe9f2d884b" />


 egrep 'Linux.*world' newfile 
### OUTPUT

<img width="378" height="88" alt="image" src="https://github.com/user-attachments/assets/59779825-d055-47c5-a1c6-e6ab6057aeab" />


 egrep 'Linux.*World' newfile 
### OUTPUT

<img width="412" height="89" alt="image" src="https://github.com/user-attachments/assets/e6e60b90-01e0-41b0-9601-5b7a23c25592" />


 egrep l{2} newfile
### OUTPUT

<img width="334" height="108" alt="image" src="https://github.com/user-attachments/assets/f888fca0-26a4-48cc-9b94-a328efb4a1dd" />


 egrep 's{1,2}' newfile
### OUTPUT 

<img width="371" height="137" alt="image" src="https://github.com/user-attachments/assets/0ef9f096-ad81-4bda-9edf-f4a5115acf27" />

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

<img width="326" height="113" alt="image" src="https://github.com/user-attachments/assets/19891bb8-1e07-44d5-87c2-1a3fe0e3d6cb" />


 sed -n -e '$p' file23
### OUTPUT

<img width="305" height="73" alt="image" src="https://github.com/user-attachments/assets/a2dadf0c-d54d-4708-8761-706fa260d235" />


 sed  -e 's/Ram/Sita/' file23
### OUTPUT

<img width="411" height="299" alt="image" src="https://github.com/user-attachments/assets/4096db39-7ad7-451d-8d75-9994d08ca571" />


 sed  -e '2s/Ram/Sita/' file23
### OUTPUT

<img width="509" height="285" alt="image" src="https://github.com/user-attachments/assets/4aa918b9-6cf3-4fbc-826b-e43d01163e9b" />


 sed  '/tom/s/5000/6000/' file23
### OUTPUT

<img width="443" height="281" alt="image" src="https://github.com/user-attachments/assets/97e41732-c801-436d-94a9-1b11c10f3414" />


 sed -n -e '1,5p' file23
### OUTPUT

<img width="354" height="199" alt="image" src="https://github.com/user-attachments/assets/4d1332f5-f94f-4484-b43b-f7eec6f5d2f4" />


 sed -n -e '2,/Joe/p' file23
### OUTPUT

<img width="401" height="159" alt="image" src="https://github.com/user-attachments/assets/8a4c99c4-2750-45ba-b84c-368b4fcc3a37" />



 sed -n -e '/tom/,/Joe/p' file23
### OUTPUT

<img width="437" height="139" alt="image" src="https://github.com/user-attachments/assets/ce810f96-760b-42fe-ae62-ddf279b26cba" />

 seq 10 | sed -n '4,6p'
### OUTPUT

<img width="458" height="124" alt="image" src="https://github.com/user-attachments/assets/2b9587f2-ebb2-42c5-95b2-6afce55f3685" />


 seq 10 | sed -n '2,~4p'
### OUTPUT

<img width="394" height="138" alt="image" src="https://github.com/user-attachments/assets/1e5d2491-3b9b-45bf-8c6f-491cf08c3d57" />


 seq 3 | sed '2a hello'
### OUTPUT

<img width="409" height="167" alt="image" src="https://github.com/user-attachments/assets/28198525-0eda-4712-9a45-0019e9703edb" />


 seq 2 | sed '2i hello'
### OUTPUT

<img width="373" height="137" alt="image" src="https://github.com/user-attachments/assets/189c07a2-e982-4b8e-829b-9db0f2f88305" />

 seq 10 | sed '2,9c hello'
### OUTPUT

<img width="410" height="132" alt="image" src="https://github.com/user-attachments/assets/22d943e7-000d-400f-b50b-fd573891d7c0" />

 sed -n '2,4{s/^/$/;p}' file23
### OUTPUT

<img width="431" height="148" alt="image" src="https://github.com/user-attachments/assets/8d9e0d14-4601-4ce6-b366-fc81c8a03c19" />


 sed -n '2,4{s/$/*/;p}' file23
### OUTPUT
<img width="450" height="167" alt="image" src="https://github.com/user-attachments/assets/c36364f1-c31f-4ece-9755-44510ad0aa9d" />


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
<img width="392" height="385" alt="image" src="https://github.com/user-attachments/assets/92f97bd0-28d8-4bbf-bcb7-82ad00522063" />


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

<img width="439" height="398" alt="image" src="https://github.com/user-attachments/assets/c7148932-9635-4738-a7ed-5abb415bf14e" />


#Using tr command

 cat file23 | tr [:lower:] [:upper:]
 ### OUTPUT

<img width="466" height="299" alt="image" src="https://github.com/user-attachments/assets/e2f15477-0ddc-402b-adef-afd2438a78c2" />

 cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
 cat < urllist.txt

<img width="426" height="289" alt="image" src="https://github.com/user-attachments/assets/95546bfe-9b19-4e06-9c40-22613bf16422" />

 cat urllist.txt | tr -d ' '
### OUTPUT

<img width="448" height="140" alt="image" src="https://github.com/user-attachments/assets/28bcd1b2-ccc6-45e0-9359-c8bf4b759ec5" />
 
 cat urllist.txt | tr -d ' ' | tr -s '.'
### OUTPUT

<img width="560" height="162" alt="image" src="https://github.com/user-attachments/assets/8bc5a719-f5c8-4059-985a-dcf3bae2f2a9" />

#Backup commands
 tar -cvf backup.tar *
### OUTPUT

<img width="398" height="324" alt="image" src="https://github.com/user-attachments/assets/68173aa9-cfc5-45e7-8bfc-4aa56ca7664f" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
### OUTPUT

<img width="593" height="323" alt="image" src="https://github.com/user-attachments/assets/5b9e2878-f133-4b69-bdf6-00e8e71bd195" />

tar -xvf backup.tar
### OUTPUT

<img width="467" height="306" alt="image" src="https://github.com/user-attachments/assets/fca6ce83-6586-4d1a-b3a3-12a27ee8902c" />

 
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

<img width="421" height="197" alt="image" src="https://github.com/user-attachments/assets/c533712e-4046-42e8-bf66-2d150a61f0ae" />


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

<img width="503" height="154" alt="image" src="https://github.com/user-attachments/assets/bb5e8c25-4058-4752-8d6e-dbd8495632ca" />


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

<img width="413" height="176" alt="image" src="https://github.com/user-attachments/assets/13b4b356-2c69-4478-8257-748e2784e90e" />

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

<img width="490" height="94" alt="image" src="https://github.com/user-attachments/assets/f0473deb-080c-4c73-b580-4f676e3728d5" />

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

<img width="427" height="150" alt="image" src="https://github.com/user-attachments/assets/b8c6527e-ffe5-4b58-bab3-ce18785208be" />

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

<img width="482" height="407" alt="image" src="https://github.com/user-attachments/assets/f6cb99ff-bc51-4c43-ab0c-2677beedcadf" />

 
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

 <img width="443" height="189" alt="image" src="https://github.com/user-attachments/assets/49df6e9d-cd38-4439-937b-444064ea8ec8" />

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

 <img width="463" height="246" alt="image" src="https://github.com/user-attachments/assets/8224e37e-a4e7-4e82-b115-6b06e7ffc978" />

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

 <img width="447" height="208" alt="image" src="https://github.com/user-attachments/assets/cd851a3e-f7c7-4cde-a4fd-2683d62b146c" />

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

 <img width="498" height="316" alt="image" src="https://github.com/user-attachments/assets/0a1df2d4-4926-4780-8234-01a68d39d049" />

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

<img width="476" height="255" alt="image" src="https://github.com/user-attachments/assets/575d1f70-0677-4028-9ee0-f9ef147fedf7" />

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

<img width="491" height="252" alt="image" src="https://github.com/user-attachments/assets/87b10d43-004e-4216-81dd-5e1a28293530" />


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

<img width="465" height="277" alt="image" src="https://github.com/user-attachments/assets/0dc99f7c-bfe9-4c56-9a2a-395c87697ec8" />

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

<img width="520" height="254" alt="image" src="https://github.com/user-attachments/assets/4bb5d752-f755-4d9f-9d77-743c295f31bf" />

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

<img width="505" height="431" alt="image" src="https://github.com/user-attachments/assets/6ae121c0-b778-4cb7-b4a5-6bdba18a9890" />

 
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

<img width="518" height="172" alt="image" src="https://github.com/user-attachments/assets/843d389c-b80e-4349-a4e1-11225520ca0e" />

 
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

<img width="614" height="270" alt="image" src="https://github.com/user-attachments/assets/c091f3ee-420a-40ba-b03e-830e5bc46a4c" />

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

<img width="622" height="158" alt="image" src="https://github.com/user-attachments/assets/13bd5b8c-f67d-4996-8816-03697363359c" />


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

<img width="548" height="196" alt="image" src="https://github.com/user-attachments/assets/a9f7b86c-e717-4f8e-9cbe-9fd5a067f18f" />
 
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
 
<img width="454" height="151" alt="image" src="https://github.com/user-attachments/assets/386e655f-e1ae-492a-9336-979e73494b47" />
<img width="472" height="103" alt="image" src="https://github.com/user-attachments/assets/c38bd157-24a3-4345-b557-6e8ad055ea53" />
 
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

 <img width="578" height="235" alt="image" src="https://github.com/user-attachments/assets/50bd2300-bce8-407f-838e-1cd3ce9399ac" />

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

<img width="561" height="504" alt="image" src="https://github.com/user-attachments/assets/e6fb0b80-df86-4733-b6f1-7ebcdc892e1d" />

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
 
 <img width="590" height="339" alt="image" src="https://github.com/user-attachments/assets/4a420690-bbd5-450f-9ffc-5e06db1e910f" />

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

<img width="558" height="421" alt="image" src="https://github.com/user-attachments/assets/dd0a9fd9-43a2-4fc9-9fb1-d544550d7c69" />

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

<img width="592" height="334" alt="image" src="https://github.com/user-attachments/assets/7cc8aa28-2a62-44c1-a577-7a8e0ab15ec2" />


# RESULT:
The Commands are executed successfully.
