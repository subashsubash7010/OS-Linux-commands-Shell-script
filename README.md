# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
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
### Display the content of the files
cat < file1
## OUTPUT

<img width="467" height="212" alt="image" src="https://github.com/user-attachments/assets/afa1912f-0eb4-433c-8987-721cb05b8d9b" />


cat < file2
## OUTPUT
<img width="475" height="261" alt="image" src="https://github.com/user-attachments/assets/5a184c00-7f74-4bec-862b-e81daf9a6243" />


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="451" height="94" alt="image" src="https://github.com/user-attachments/assets/2432fe6c-f9dc-48f1-96db-480f319895c5" />

comm file1 file2
 ## OUTPUT

 
diff file1 file2
## OUTPUT
<img width="621" height="419" alt="image" src="https://github.com/user-attachments/assets/0a3dea28-a1cd-42e4-8bb8-6f5a7ad0e55f" />


#Filters

### Create the following files file11, file22 as follows:

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
## OUTPUT


<img width="465" height="88" alt="image" src="https://github.com/user-attachments/assets/7e53e886-95cd-4f57-9a5f-2d3c1f4010a2" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="404" height="176" alt="image" src="https://github.com/user-attachments/assets/91839865-6817-4a2f-a16b-bcf188d597a3" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="524" height="146" alt="image" src="https://github.com/user-attachments/assets/b52aef80-a86f-4b14-a29d-1bfd95664e96" />

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="513" height="89" alt="image" src="https://github.com/user-attachments/assets/5bdf25e9-3eb7-46d9-a308-61b76b4d4c4c" />


grep hello newfile 
## OUTPUT

<img width="471" height="93" alt="image" src="https://github.com/user-attachments/assets/565d7a30-bd81-4952-8230-217b3f2f176c" />



grep -v hello newfile 
## OUTPUT

<img width="496" height="96" alt="image" src="https://github.com/user-attachments/assets/62bbd738-4cd4-45d0-ae11-8c07e23ecab8" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="602" height="114" alt="image" src="https://github.com/user-attachments/assets/ff240969-a377-42ce-8de3-c51e5ac78457" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="555" height="86" alt="image" src="https://github.com/user-attachments/assets/e36a956b-b0d6-4c81-9c8b-1f2303009c89" />



grep -R ubuntu /etc
## OUTPUT

<img width="530" height="126" alt="image" src="https://github.com/user-attachments/assets/f1e0c8fa-71bb-4299-9f7a-98d006b9e55b" />


grep -w -n world newfile   
## OUTPUT

<img width="576" height="125" alt="image" src="https://github.com/user-attachments/assets/a743733f-cbf0-4717-b5a7-5475f2560a6b" />

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
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="529" height="122" alt="image" src="https://github.com/user-attachments/assets/2456bf62-d8eb-4c9a-859b-772e6ac83e10" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="520" height="122" alt="image" src="https://github.com/user-attachments/assets/534b469e-902e-4a7e-bd4a-b1fc9bb904f8" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="566" height="135" alt="image" src="https://github.com/user-attachments/assets/adbd715e-1e1c-4039-9dba-f07fb0f6b12b" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="499" height="96" alt="image" src="https://github.com/user-attachments/assets/44aa0ba7-c6f7-48e2-9b6f-b3d317bd82b2" />


egrep '(world$)' newfile 
## OUTPUT

<img width="480" height="129" alt="image" src="https://github.com/user-attachments/assets/53513133-606d-4e80-9085-b768e812229e" />


egrep '(World$)' newfile 
## OUTPUT

<img width="532" height="100" alt="image" src="https://github.com/user-attachments/assets/722485b6-9939-4057-a89d-19db2cf1cc96" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="562" height="150" alt="image" src="https://github.com/user-attachments/assets/f6fb7492-40e0-490e-b958-07984350c1e7" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="608" height="91" alt="image" src="https://github.com/user-attachments/assets/5cad67d4-61a7-4df8-9bcc-d07a5b793721" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="533" height="92" alt="image" src="https://github.com/user-attachments/assets/02775827-5efc-4bf5-b91f-9d0291d97e0c" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="584" height="93" alt="image" src="https://github.com/user-attachments/assets/d7e6e029-4f74-471c-9f34-e786e69f13c7" />

egrep l{2} newfile
## OUTPUT

<img width="472" height="115" alt="image" src="https://github.com/user-attachments/assets/a8c300a7-18fa-48ec-b362-2c36a67fb94c" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="563" height="149" alt="image" src="https://github.com/user-attachments/assets/0e5b39bc-128e-4618-a5a5-721b01f56e21" />


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
## OUTPUT

<img width="503" height="93" alt="image" src="https://github.com/user-attachments/assets/97d2aa2a-612f-4fae-b228-8cd1384b00c5" />


sed -n -e '$p' file23
## OUTPUT

<img width="452" height="92" alt="image" src="https://github.com/user-attachments/assets/c6d24ffe-6e40-4d42-9c29-1d198273d80a" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="620" height="298" alt="image" src="https://github.com/user-attachments/assets/73dfd3e8-4cc8-4950-8a1a-a69f3a4711da" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="470" height="334" alt="image" src="https://github.com/user-attachments/assets/1435b849-0780-49e3-9af0-885b3792ada1" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="501" height="219" alt="image" src="https://github.com/user-attachments/assets/2398dcda-22d9-447f-b938-8567e4b13665" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="609" height="127" alt="image" src="https://github.com/user-attachments/assets/8f722b84-594f-4728-85e6-fbdb53c2458e" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="484" height="154" alt="image" src="https://github.com/user-attachments/assets/c244b823-4fa5-4c9f-8188-c908599a341d" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="582" height="153" alt="image" src="https://github.com/user-attachments/assets/94ba7fbd-18e0-4275-8e2d-9e16bba69042" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="404" height="180" alt="image" src="https://github.com/user-attachments/assets/58b6e6da-9240-46d0-8360-99e2666f51dc" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="439" height="158" alt="image" src="https://github.com/user-attachments/assets/21bc4128-142d-4b2e-9ac1-69f26b01c82d" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="444" height="148" alt="image" src="https://github.com/user-attachments/assets/1a30a535-087e-4b7e-9035-fdd4cc567bc3" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="665" height="153" alt="image" src="https://github.com/user-attachments/assets/9a78e57f-a342-4bbf-b2e9-93bc115c5d5f" />


sed -n '2,4{s/$/*/;p}' file23
<img width="589" height="148" alt="image" src="https://github.com/user-attachments/assets/20d56c1d-d48b-4724-b743-03e44a433ee8" />


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
## OUTPUT

<img width="546" height="210" alt="image" src="https://github.com/user-attachments/assets/bff2c5c0-4ee1-46b2-923f-c962944fab83" />

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
## OUTPUT

<img width="563" height="219" alt="image" src="https://github.com/user-attachments/assets/0cb40898-5356-492b-908f-5164b6878c24" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

 <img width="650" height="307" alt="image" src="https://github.com/user-attachments/assets/05dc46d1-754e-4997-9986-8cb49b136e6f" />


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT


 <img width="613" height="150" alt="image" src="https://github.com/user-attachments/assets/2608116a-8e6c-4d50-8024-6e5a69cbb15c" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="596" height="151" alt="image" src="https://github.com/user-attachments/assets/21784abb-4112-4da2-9e0d-8f49a3d6cb77" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="704" height="631" alt="image" src="https://github.com/user-attachments/assets/3a14301b-cf36-4212-8ef5-a3cae0f15ca9" />

<img width="849" height="729" alt="image" src="https://github.com/user-attachments/assets/6dcb533c-c384-4478-9226-06c2ed1805fc" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="938" height="777" alt="image" src="https://github.com/user-attachments/assets/711a3c57-4877-48f3-ada2-96f160438618" />
<img width="945" height="804" alt="image" src="https://github.com/user-attachments/assets/f6ae6e5a-9b44-4588-a4ba-7a6e1ac8e3e5" />


tar -xvf backup.tar
## OUTPUT

<img width="899" height="654" alt="image" src="https://github.com/user-attachments/assets/e42041e4-62f2-434e-81ed-1e6004d63329" />
<img width="900" height="667" alt="image" src="https://github.com/user-attachments/assets/6bb25caa-41b9-4b91-9ae9-aebc64b1c7a6" />

gzip backup.tar
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="596" height="70" alt="image" src="https://github.com/user-attachments/assets/d22291ba-e073-4b64-8435-9aae5616f6a7" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="590" height="187" alt="image" src="https://github.com/user-attachments/assets/7f42e885-1c1c-4d44-bb76-fe3fd3fa639f" />


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

## OUTPUT
<img width="773" height="480" alt="image" src="https://github.com/user-attachments/assets/0cf79877-bedb-465d-be08-94e76c2a5c33" />

 
ls file1
## OUTPUT

<img width="652" height="101" alt="image" src="https://github.com/user-attachments/assets/0b34dc25-b0fa-4939-b40a-b25a20bd8447" />

echo $?
## OUTPUT 

<img width="585" height="89" alt="image" src="https://github.com/user-attachments/assets/ef9f642c-f623-4962-bd5b-14023a65d831" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="529" height="95" alt="image" src="https://github.com/user-attachments/assets/c7f326b4-9e59-496f-8166-a4b1d5a6edbb" />

echo $?
 ## OUTPUT

<img width="1" height="1" alt="image" src="https://github.com/user-attachments/assets/0535bac4-bbfb-4e06-9d38-c49928dff662" />

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
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
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT


<img width="902" height="659" alt="image" src="https://github.com/user-attachments/assets/286a462a-697a-4590-82c7-5058a612ede8" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="880" height="128" alt="image" src="https://github.com/user-attachments/assets/a48a11a3-5ec5-47ba-b74a-70c4a7958778" />


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
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
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
e se
echo “Sorry, you are not the owner of the /etc/passwd fil
fi
 ```
./psswdperm.sh
## OUTPUT

<img width="798" height="100" alt="image" src="https://github.com/user-attachments/assets/91243637-d9e0-4c79-8fee-2b64936064aa" />

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
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
\#!/bin/bash
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
## OUTPUT

<img width="640" height="93" alt="image" src="https://github.com/user-attachments/assets/0cba6c48-32d0-431c-a88c-70b250091c87" />


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
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
\#!/bin/bash
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

<img width="761" height="155" alt="image" src="https://github.com/user-attachments/assets/a9072e38-854c-415f-a08a-2f4fca534140" />

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
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
\#!/bin/bash
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

<img width="837" height="209" alt="image" src="https://github.com/user-attachments/assets/b4a780d2-48ac-498f-91f0-f8bf56bc265d" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
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
 


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="559" height="157" alt="image" src="https://github.com/user-attachments/assets/b9ec9232-6ff3-455b-aee3-4e8a914d11e4" />

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
## Output

 <img width="547" height="160" alt="image" src="https://github.com/user-attachments/assets/435b7ab6-4838-4324-80b7-824ed25970e2" />


cat > whiletest
```bash
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
 ## Output
 <img width="506" height="365" alt="image" src="https://github.com/user-attachments/assets/0514178d-1dec-4827-9126-90fae656c047" />

 
cat untiltest.sh 
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
 
## output


<img width="501" height="181" alt="image" src="https://github.com/user-attachments/assets/7ec987c3-63ad-4da4-b116-2d82fa5c0e60" />

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin1.sh 

## Output

<img width="818" height="235" alt="image" src="https://github.com/user-attachments/assets/1210a94b-108f-4de9-b019-a1967ea89061" />

```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 

## Output 

<img width="695" height="239" alt="image" src="https://github.com/user-attachments/assets/7f0afeed-1f40-42b4-b9be-f7ad35696760" />

```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 


## Output 
<img width="812" height="244" alt="image" src="https://github.com/user-attachments/assets/2e1d2c7c-6acb-4e35-9d88-a886b6c2fa87" />

```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
## Output 

<img width="829" height="234" alt="image" src="https://github.com/user-attachments/assets/b917c95c-9b76-4c36-95e4-bc2ca1853377" />

$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

<img width="471" height="275" alt="image" src="https://github.com/user-attachments/assets/09824a00-0805-4fdc-8c07-4d9bd87fb8d8" />


cat forin6.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forin6.sh
$ ./forin6.sh 
## OUTPUT


<img width="499" height="218" alt="image" src="https://github.com/user-attachments/assets/e4b25543-a1c9-4e8b-8116-56bbc61bff2b" />

cat forctype1.sh 
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
## Outpput

<img width="498" height="226" alt="image" src="https://github.com/user-attachments/assets/08a60784-3025-48f7-95da-65d019331213" />


cat fornested1.sh 
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
 ## OUTPUT

 <img width="615" height="426" alt="image" src="https://github.com/user-attachments/assets/7f8af9cf-8378-4180-b548-e24669f86f02" />

cat forbreak.sh 

```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
## OUTPUT

<img width="893" height="156" alt="image" src="https://github.com/user-attachments/assets/04ad318b-74fc-474f-9a80-7fd4630fb895" />

cat forbreak.sh 
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
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="887" height="208" alt="image" src="https://github.com/user-attachments/assets/daf93e57-9836-4928-b460-8e8e9f582ac5" />

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT

<img width="743" height="173" alt="image" src="https://github.com/user-attachments/assets/4944ef20-ba82-45fd-b1c4-8e85c2e5ce0e" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 

## OUTPUT

<img width="807" height="121" alt="image" src="https://github.com/user-attachments/assets/cd9fb1ca-1e36-4629-a031-e1270595b982" />


cat funcex.sh
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

 ./funcex.sh 
## OUTPUT

<img width="567" height="105" alt="image" src="https://github.com/user-attachments/assets/f27b17bc-c1fe-4cb0-a729-5da4fd4871ed" />


cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3

## OUTPUT

<img width="582" height="156" alt="image" src="https://github.com/user-attachments/assets/b621dbf3-e486-4451-b223-536b278b77fb" />


 cat argshift1.sh
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

## OUTPUT

<img width="582" height="156" alt="image" src="https://github.com/user-attachments/assets/76d5d209-0050-4ab8-9840-e355e3adf8fe" />


cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
./argshift.sh 1 2 3

## OUTPUT

 <img width="582" height="156" alt="image" src="https://github.com/user-attachments/assets/0d33c84c-4df6-4c9e-a7c2-793fba3ed937" />

 
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
## OUTPUT 

<img width="666" height="448" alt="image" src="https://github.com/user-attachments/assets/974f8cde-e3e3-478c-b071-c8c6ca260652" />

 
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
## OUTPUT 

<img width="691" height="160" alt="image" src="https://github.com/user-attachments/assets/f3860b32-ae31-4a50-849e-7522f5b011bd" />


# RESULT:
The Commands are executed successfully.
