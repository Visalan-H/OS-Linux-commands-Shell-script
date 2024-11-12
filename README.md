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
<img src="https://github.com/user-attachments/assets/4300bbc2-a58e-4301-8d9e-f70bc9f609f9" width="350px">

cat < file2
## OUTPUT
<img src="https://github.com/user-attachments/assets/51b6d8d0-cf7b-48d6-a754-d365ed94d745" width="350px">

# Comparing Files
cmp file1 file2
## OUTPUT
<img src="https://github.com/user-attachments/assets/e2e5b8fe-63f6-4f88-988c-499a92f2a23b" width="350px">

comm file1 file2
 ## OUTPUT
<img src="https://github.com/user-attachments/assets/e3a14a85-c487-488e-add4-0463f7664ade" width="350px">

diff file1 file2
## OUTPUT
<img src="https://github.com/user-attachments/assets/ec89ed66-16c1-4907-9fbf-78aef5e2a7ea" width="350px">

# Filters

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
<img src="https://github.com/user-attachments/assets/c429d78c-a5ee-4435-acd3-1cf71a5959bd" width="350px">

cut -d "|" -f 1 file22
## OUTPUT
<img src="https://github.com/user-attachments/assets/63b3a3ae-09b0-46ec-a243-818a8b29e5cc" width="350px">

cut -d "|" -f 2 file22
## OUTPUT
<img src="https://github.com/user-attachments/assets/020f3673-eaa5-4c44-b650-1604b769cb03" width="350px">

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
<img src="https://github.com/user-attachments/assets/aad532b2-8bd7-41f1-b116-41f1e4d81a03" width="350px">

grep hello newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/b73194a1-d4b3-4d69-82b6-5ebb97e55f0d" width="350px">

grep -v hello newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/7c206c40-14bf-41df-b6a6-31b7cbc6a993" width="350px">

cat newfile | grep -i "hello"
## OUTPUT
<img src="https://github.com/user-attachments/assets/eef14ba5-f2b0-4ef3-a789-82f57841e4de" width="350px">

cat newfile | grep -i -c "hello"
## OUTPUT
<img src="https://github.com/user-attachments/assets/20b5cbb4-2a4a-423d-8b1d-fa84e0bc52c9" width="350px">

grep -R ubuntu /etc
## OUTPUT
<img src="https://github.com/user-attachments/assets/975dce95-3309-4d93-b77c-0d7080b2f5c7" width="350px">

grep -w -n world newfile   
## OUTPUT
<img src="https://github.com/user-attachments/assets/1b8747b8-370d-4e9f-a84c-de847c5a1a54" width="350px">


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

<img src="https://github.com/user-attachments/assets/ddb630a2-5bae-4f66-972d-54953dc23f39" width="350px">


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/006d984c-e67d-42e1-80e4-52769727dcbe" width="350px">

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/240cf640-6c8a-4ab1-b7f3-f9d7e21b1bfa" width="350px">

egrep '(^hello)' newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/f120824e-3c7b-41e3-848d-cd2d26d54b47" width="350px">

egrep '(world$)' newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/ace1db4c-d90e-4b7a-8273-d4c9b56b5e86" width="350px">

egrep '(World$)' newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/94f276a3-85da-4907-876e-1d4649460c57" width="350px">


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img src="https://github.com/user-attachments/assets/2af455e5-364d-4941-87c2-3de49a319f46" width="350px">


egrep '[1-9]' newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/78500f6f-66da-402d-973b-c7a62d6e95e5" width="350px">


egrep 'Linux.*world' newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/2dccc17b-fde9-473f-9719-60cc2bedcd14" width="350px">


egrep 'Linux.*World' newfile 
## OUTPUT
<img src="https://github.com/user-attachments/assets/747aa98e-e2df-4512-88e3-24a3b8a62ede" width="350px">


egrep l{2} newfile
## OUTPUT
<img src="https://github.com/user-attachments/assets/b4216d99-7a58-429f-81ff-365c043b6365" width="350px">


egrep 's{1,2}' newfile
## OUTPUT 
<img src="https://github.com/user-attachments/assets/183ca2b0-3391-45d3-b9cd-ff014012245a" width="350px">


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
<img src="https://github.com/user-attachments/assets/37170438-bec8-4728-8697-59aae8596bc7" width="350px">


sed -n -e '$p' file23
## OUTPUT
<img src="https://github.com/user-attachments/assets/c755ea4b-bf58-401e-aedc-0d32fdd5a240" width="350px">

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img src="https://github.com/user-attachments/assets/69fdebd7-00b1-4755-a258-4d2a87e1cdcc" width="350px">


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img src="https://github.com/user-attachments/assets/62929cd3-68cc-4648-828c-afa2ca34effb" width="350px">



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img src="https://github.com/user-attachments/assets/ce623e0d-d4cd-4150-b6c6-c7e81cc5185f" width="350px">



sed -n -e '1,5p' file23
## OUTPUT
<img src="https://github.com/user-attachments/assets/8a5e7d06-b001-40b5-9141-f7c01dee7ca9" width="350px">



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img src="https://github.com/user-attachments/assets/0eacbc01-48f3-4f10-866a-fea0757405b3" width="350px">




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img src="https://github.com/user-attachments/assets/e9820e8d-6d6a-4ebb-ba48-403459dbba66" width="350px">

seq 10 
## OUTPUT
<img src="https://github.com/user-attachments/assets/b7900823-b355-4093-9b98-73c77306ddba" width="350px">



seq 10 | sed -n '4,6p'
## OUTPUT

<img src="https://github.com/user-attachments/assets/f53e2d75-fa67-422d-8df6-7fbb83c506d2" width="350px">

seq 10 | sed -n '2,~4p'
## OUTPUT
<img src="https://github.com/user-attachments/assets/927b0a13-3b07-425f-9114-0c39790a8e49" width="350px">

seq 3 | sed '2a hello'
## OUTPUT
<img src="https://github.com/user-attachments/assets/8c7fd082-6b35-4969-aac8-81abaea317b0" width="350px">



seq 2 | sed '2i hello'
## OUTPUT
<img src="https://github.com/user-attachments/assets/b696fc13-5a4c-4af4-823f-29c96bb891a0" width="350px">


seq 10 | sed '2,9c hello'
## OUTPUT
<img src="https://github.com/user-attachments/assets/d23ed611-370f-4981-9755-e264d8b50359" width="350px">

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img src="https://github.com/user-attachments/assets/302da326-2c04-4a8f-85af-ede0dad28fe8" width="350px">

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img src="https://github.com/user-attachments/assets/d682c5a7-0e2d-4d23-91b7-e08893cb0196" width="350px">

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
<img src="https://github.com/user-attachments/assets/e941cfb1-c566-418f-9a54-32e19963b8da" width="350px">

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
<img src="https://github.com/user-attachments/assets/167e44aa-e4e8-4051-92a1-0b8164cfcf3a" width="350px">

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img src="https://github.com/user-attachments/assets/e393f123-4d99-4741-a09b-2fa81b1a38ca" width="350px">

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
	
<img src="https://github.com/user-attachments/assets/dbab3a4a-798f-4e34-91f3-63cce09a0808" width="350px">

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img src="https://github.com/user-attachments/assets/c9e79d98-9ae9-470a-8bf4-d074462992b2" width="350px">

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img src="https://github.com/user-attachments/assets/11e9a3b0-d33f-44e9-a31e-129bb4920ecd" width="350px">

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
<img src="https://github.com/user-attachments/assets/987b8f9f-9128-40b1-9928-926489603cd0" width="350px">

tar -xvf backup.tar
## OUTPUT
<img src="https://github.com/user-attachments/assets/9da5f757-cc7e-4647-9c42-b926e90dcf36" width="350px">

gzip backup.tar

ls .gz
## OUTPUT
<!-- ![image](https://github.com/user-attachments/assets/f1f69d77-7f78-4c1c-80ef-edc309cf0a04) -->

<!-- ![image](https://github.com/user-attachments/assets/ebb7917a-abdd-409d-93cb-27583f6ebcc7)
-->

gunzip backup.tar.gz
## OUTPUT
<img src="https://github.com/user-attachments/assets/7867265a-25f0-44e7-8f7c-41c337095a1f" width="350px">
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img src="https://github.com/user-attachments/assets/e5fb4faa-5268-4af2-bd10-93952a3df02f" width="350px">

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
<img src="https://github.com/user-attachments/assets/c41df452-740c-4904-ae37-e051e2f45c33" width="350px">

ls file1
## OUTPUT
<img src="https://github.com/user-attachments/assets/c0160adc-e299-4218-9cf3-847f54708d47" width="350px">

echo $?

## OUTPUT 
<img src="https://github.com/user-attachments/assets/6d889bd0-f3e2-4452-8e03-f7cb2221c080" width="350px">

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img src="https://github.com/user-attachments/assets/e664eab6-d7a4-4382-b449-f401ac12b9f8" width="350px">

abcd

 ![image](https://github.com/user-attachments/assets/9fe44fdc-b2ba-4d60-a19f-423e076bc1d6)

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
## OUTPUT

<img src="https://github.com/user-attachments/assets/a5e4ba2c-255e-4a15-852f-12b373f61991" width="350px">


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img src="https://github.com/user-attachments/assets/f2b3a632-6b40-45d0-9563-cc6f56e6c43a" width="350px">

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
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

<img src="https://github.com/user-attachments/assets/2e1d0e9e-da38-4fc1-bd7b-3885f04b77a7" width="350px">

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

<img src="https://github.com/user-attachments/assets/a69909c7-6d9a-406d-ad47-c22dfe4a0b52" width="350px">

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
## OUTPUT

<img src="https://github.com/user-attachments/assets/9f7b770d-4f8b-4a35-9717-689c211536af" width="350px">

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
## OUTPUT
<img src="https://github.com/user-attachments/assets/b5c7122d-8897-4bcb-97c6-d1aa605bda61" width="350px">

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
 
$ ./elifcheck.sh 
## OUTPUT
<img src="https://github.com/user-attachments/assets/7b827572-b943-4ce4-bf3c-49fee5043937" width="350px">

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

<img src="https://github.com/user-attachments/assets/d4df5c7a-389f-4c3d-84e5-68587e5998dc" width="350px">

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

<img src="https://github.com/user-attachments/assets/728f52d8-adc6-4c45-bdec-2e8d2f869428" width="350px">

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
## OUTPUT
<img src="https://github.com/user-attachments/assets/611be04f-3458-4636-a0a7-33f9adf761ba" width="350px">

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
 
 ## OUTPUT
<img src="https://github.com/user-attachments/assets/71ecc863-8c9c-4a93-a1b7-275c9c742bcb" width="350px">
 
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
 ## OUTPUT
 ![image](https://github.com/user-attachments/assets/8ff70871-37bf-4c48-9a5f-915a896fb71d)

 
cat forin2.sh 
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
<img src="https://github.com/user-attachments/assets/9fe44fdc-b2ba-4d60-a19f-423e076bc1d6" width="350px">

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
## OUTPUT
![image](https://github.com/user-attachments/assets/a0c35913-b1dd-4fd6-b906-3f12d7c363ac)

 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh
![image](https://github.com/user-attachments/assets/c6367cff-7ab7-492d-bfe5-573ad50fc630)

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
![image](https://github.com/user-attachments/assets/d5f272ae-27b0-43c9-a336-487d61deb265)


cat forctype.sh 
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
## OUTPUT

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
## OUTPUT
![image](https://github.com/user-attachments/assets/16603047-f339-47bb-8716-35e38cf2a6a3)

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
![image](https://github.com/user-attachments/assets/cf913aeb-06b0-48f2-ae31-4d5beb2cce07)

 
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
![image](https://github.com/user-attachments/assets/d6db6d77-e884-4309-bb58-155533da390a)

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
 ![image](https://github.com/user-attachments/assets/34fd141e-16e1-4e9c-90d8-026617518c11)

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
![image](https://github.com/user-attachments/assets/d5234e31-ee07-4d34-b657-e871bbc73a45)


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
![image](https://github.com/user-attachments/assets/b3d2e24e-0ecc-4457-be47-65aa923ddc0e)
 
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
## OUTPUT
 ./funcex.sh 
![image](https://github.com/user-attachments/assets/8b4c1b78-1f92-4151-bc4e-9f033cdd6cef)

 
 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/54181cb2-3adf-4276-8489-6e02236be56a)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
![image](https://github.com/user-attachments/assets/f71780d2-ccf7-4c99-a130-9a21d4d98f1f)

 
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
## OUTPUT
$ ./argshift.sh 1 2 3
 ![image](https://github.com/user-attachments/assets/d750bbfb-fc92-4439-908d-6896001e889b)

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
## OUTPUT
 ./argshift.sh 1 2 3
 ![image](https://github.com/user-attachments/assets/ca05469e-6b80-480f-a01d-b2975dade444)

 
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
 ![image](https://github.com/user-attachments/assets/44654b99-b394-4c8a-b1b3-3e6b5966f5a1)

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
![image](https://github.com/user-attachments/assets/b2d33953-e600-4c30-9df0-5c0ed57920aa)


# RESULT:
The Commands are executed successfully.
