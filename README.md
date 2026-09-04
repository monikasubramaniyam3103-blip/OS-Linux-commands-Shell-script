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

<img width="420" height="121" alt="image" src="https://github.com/user-attachments/assets/1c8e8eb3-dea7-4a0e-ab37-e9fc3ff726da" />


cat < file2
## OUTPUT

<img width="446" height="181" alt="image" src="https://github.com/user-attachments/assets/40b6a3be-f790-4102-9d22-88489ac39366" />

# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="491" height="50" alt="image" src="https://github.com/user-attachments/assets/2a78f99a-e9a5-4a09-9967-7bc8090d47ab" />

comm file1 file2
 ## OUTPUT
<img width="491" height="50" alt="image" src="https://github.com/user-attachments/assets/ebb56c11-0540-43b3-b758-ac34009ca5e9" />

 
diff file1 file2
## OUTPUT

<img width="574" height="349" alt="image" src="https://github.com/user-attachments/assets/8883102e-2947-48e3-9c46-7fd5cd1c4482" />


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


<img width="457" height="102" alt="image" src="https://github.com/user-attachments/assets/db1230af-6d94-4850-ac4e-d4986b540430" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="490" height="122" alt="image" src="https://github.com/user-attachments/assets/016007f2-c586-4a55-915e-26e2b6d9ed6e" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="516" height="132" alt="image" src="https://github.com/user-attachments/assets/b3922397-37f1-4606-8639-4f328ea8ad7e" />


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

<img width="520" height="70" alt="image" src="https://github.com/user-attachments/assets/86aa1a87-04aa-48cd-bb4a-ecdb5ed830aa" />


grep hello newfile 
## OUTPUT


<img width="482" height="62" alt="image" src="https://github.com/user-attachments/assets/323281c9-c6fd-4008-8b63-52ff700bda65" />


grep -v hello newfile 
## OUTPUT

<img width="513" height="77" alt="image" src="https://github.com/user-attachments/assets/4d18ec30-afe6-48c4-9d02-29a2dca1a293" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="638" height="97" alt="image" src="https://github.com/user-attachments/assets/75616586-290c-4155-b93a-be6a3d8de2ac" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="692" height="69" alt="image" src="https://github.com/user-attachments/assets/eacefad1-9586-4c93-b61e-392cb1c6abc8" />



grep -R ubuntu /etc
## OUTPUT

<img width="745" height="238" alt="image" src="https://github.com/user-attachments/assets/4966e06f-d876-41c5-bb22-1474511fdaa4" />


grep -w -n world newfile   
## OUTPUT
<img width="717" height="99" alt="image" src="https://github.com/user-attachments/assets/980fcc23-3fc5-487d-8b7b-b623a64d0b19" />


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

<img width="726" height="96" alt="image" src="https://github.com/user-attachments/assets/6ff72594-8bca-48b0-9e62-5b331e514f2c" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="627" height="89" alt="image" src="https://github.com/user-attachments/assets/c9728a0a-9351-4b73-aa4d-f148fcfd538a" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="698" height="88" alt="image" src="https://github.com/user-attachments/assets/a0ce0c6c-2863-4a70-a59f-2f5dcf777378" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="581" height="60" alt="image" src="https://github.com/user-attachments/assets/55d36533-012a-4f2b-a511-d4e08c1ff586" />


egrep '(world$)' newfile 
## OUTPUT

<img width="581" height="60" alt="image" src="https://github.com/user-attachments/assets/16558083-76bc-498c-aca3-a25a76e089dc" />


egrep '(World$)' newfile 
## OUTPUT

<img width="608" height="66" alt="image" src="https://github.com/user-attachments/assets/316d3f25-e3ca-4a04-a598-77d99cb62216" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="605" height="92" alt="image" src="https://github.com/user-attachments/assets/9959a526-fbbc-4782-9763-715b7c28595f" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="592" height="68" alt="image" src="https://github.com/user-attachments/assets/69702fad-7502-4a05-8a0f-e99ff26ddad0" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="644" height="69" alt="image" src="https://github.com/user-attachments/assets/45fb510e-6f03-4c75-ad55-e2d6ca7482c6" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="619" height="64" alt="image" src="https://github.com/user-attachments/assets/f46302d0-c168-4adc-93dc-cd6c147ce9c5" />

egrep l{2} newfile
## OUTPUT

<img width="727" height="98" alt="image" src="https://github.com/user-attachments/assets/564e2473-eced-493f-bbcb-36a1caaefa72" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="732" height="128" alt="image" src="https://github.com/user-attachments/assets/fb041f95-2865-431b-a590-0f39de53bb60" />

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

<img width="514" height="59" alt="image" src="https://github.com/user-attachments/assets/a695bf90-7328-410f-abb0-0747dabe1b1c" />


sed -n -e '$p' file23
## OUTPUT

<img width="536" height="64" alt="image" src="https://github.com/user-attachments/assets/875c454b-d7b7-45a4-aeed-1ff1b4bd76a2" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="592" height="263" alt="image" src="https://github.com/user-attachments/assets/9ea400b6-e128-4f78-8a68-37b43f58c07e" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="595" height="272" alt="image" src="https://github.com/user-attachments/assets/3a0c8979-c1ab-49a3-b218-89a7105de753" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="648" height="278" alt="image" src="https://github.com/user-attachments/assets/40d24f8f-6920-4517-adb9-15a0c487a791" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="592" height="180" alt="image" src="https://github.com/user-attachments/assets/6cea799b-1945-41eb-ad3e-e31d8a4dc648" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="581" height="119" alt="image" src="https://github.com/user-attachments/assets/7d3a9bf5-2e52-4fdb-815e-1f68a4be4aca" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="636" height="86" alt="image" src="https://github.com/user-attachments/assets/fa4fd2e5-ac0c-4237-acea-bb1224069c08" />


seq 10 
## OUTPUT

<img width="556" height="335" alt="image" src="https://github.com/user-attachments/assets/a2275924-c9f3-4ec2-acf5-8a65ee89911e" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="548" height="120" alt="image" src="https://github.com/user-attachments/assets/ddf356a6-e75b-4af4-aa67-e57741ffa4f9" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="554" height="119" alt="image" src="https://github.com/user-attachments/assets/ed198776-92d8-4f54-a4fb-3a6abc530a6c" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="561" height="119" alt="image" src="https://github.com/user-attachments/assets/cf839ebe-5d2f-4fb4-b162-cb425f6e8695" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="562" height="144" alt="image" src="https://github.com/user-attachments/assets/dc1767e5-a47c-4791-967b-331e6e5cf18a" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="570" height="119" alt="image" src="https://github.com/user-attachments/assets/d67cc42a-ecbb-4b06-9b21-a5a39c737371" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="573" height="104" alt="image" src="https://github.com/user-attachments/assets/7d86727a-a82a-414a-a0ee-45e7a1d50ba3" />


sed -n '2,4{s/$/*/;p}' file23
<img width="609" height="122" alt="image" src="https://github.com/user-attachments/assets/7377e37f-6092-4f8f-92cb-c90fabcbb5f5" />


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

<img width="406" height="189" alt="image" src="https://github.com/user-attachments/assets/04c289f7-8804-434b-8628-ce2d95335fd5" />

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

<img width="380" height="175" alt="image" src="https://github.com/user-attachments/assets/3b3506a8-cfae-4c31-a9bc-47cc60a8b284" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="694" height="258" alt="image" src="https://github.com/user-attachments/assets/f7c9a613-7b21-4cad-8db8-ca176bc3ff5f" />

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

<img width="634" height="114" alt="image" src="https://github.com/user-attachments/assets/12282e2c-52eb-4f1b-8b02-927f884ddbf2" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="746" height="120" alt="image" src="https://github.com/user-attachments/assets/7159df9c-0970-4cb6-95fe-0a745242cff9" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="367" height="89" alt="image" src="https://github.com/user-attachments/assets/e92e598e-de99-4e6a-a196-57b0e5a3f16c" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="288" height="86" alt="image" src="https://github.com/user-attachments/assets/a24daef8-d3af-4df4-8c1b-8cd67d2e09f3" />


tar -xvf backup.tar
## OUTPUT
<img width="766" height="147" alt="image" src="https://github.com/user-attachments/assets/661602d4-19ba-458c-bef4-ba7f6cc72c1e" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="764" height="156" alt="image" src="https://github.com/user-attachments/assets/7e6f201b-e10f-4dad-ad23-19c936a8fe76" />
 
gunzip backup.tar.gz
## OUTPUT

<img width="767" height="222" alt="image" src="https://github.com/user-attachments/assets/472c2c77-5bf6-40a2-ae60-f0550a14a976" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="750" height="313" alt="image" src="https://github.com/user-attachments/assets/6aee3c85-a5ed-4716-a4cd-4349097a7a24" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="433" height="122" alt="image" src="https://github.com/user-attachments/assets/10bd3dec-8b47-4f40-98ff-1291e30ff5ff" />


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
<img width="538" height="433" alt="image" src="https://github.com/user-attachments/assets/38a16c5a-8eb9-40ab-bc17-d21b2aaeacac" />

 
ls file1
## OUTPUT
<img width="324" height="56" alt="image" src="https://github.com/user-attachments/assets/0dd1e781-de62-442d-9508-d309eea61db6" />

echo $?
## OUTPUT 

<img width="314" height="65" alt="image" src="https://github.com/user-attachments/assets/72242ad1-4ff9-48ea-a02f-24e26236b5a1" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT

<img width="316" height="64" alt="image" src="https://github.com/user-attachments/assets/c9871e0d-bf50-490b-9e00-943330289889" />

abcd
 
echo $?
 ## OUTPUT

<img width="652" height="299" alt="image" src="https://github.com/user-attachments/assets/f6b0a98a-38be-4137-ae4c-ed7ea1c6f94f" />

 
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

<img width="641" height="328" alt="image" src="https://github.com/user-attachments/assets/24156e50-a15d-4ecd-beee-6249246244ff" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="781" height="316" alt="image" src="https://github.com/user-attachments/assets/4c262d79-2f24-4238-9849-47ad7f340632" />


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

<img width="777" height="233" alt="image" src="https://github.com/user-attachments/assets/684f3c45-6095-400c-a5f2-571682db3449" />

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

<img width="685" height="543" alt="image" src="https://github.com/user-attachments/assets/1623c92b-a401-46bd-80af-c69ddf02111e" />


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

<img width="729" height="648" alt="image" src="https://github.com/user-attachments/assets/e9aca479-6e94-4f4a-adbd-70dcfba1433e" />


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

<img width="759" height="653" alt="image" src="https://github.com/user-attachments/assets/faf6d8fd-ebe1-448b-98f2-e3ad22a51b32" />


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

<img width="755" height="636" alt="image" src="https://github.com/user-attachments/assets/f4a08f7d-9d9c-4ee8-8d18-3132d03038ff" />

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

<img width="682" height="341" alt="image" src="https://github.com/user-attachments/assets/facc7609-e534-4674-83a1-a53c48f71fc8" />

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

 <img width="525" height="267" alt="image" src="https://github.com/user-attachments/assets/48824675-5594-4c28-bcdb-5d66f945f91d" />

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

<img width="513" height="275" alt="image" src="https://github.com/user-attachments/assets/d2085c3f-326e-4e99-ade9-681dd7b40098" />

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

<img width="775" height="290" alt="image" src="https://github.com/user-attachments/assets/92dde098-57a4-4572-a66d-205c58bc18c4" />

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
<img width="513" height="275" alt="image" src="https://github.com/user-attachments/assets/24aeb988-a454-40f6-8080-f20cf2441b8c" />

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
<img width="769" height="286" alt="image" src="https://github.com/user-attachments/assets/85cf7070-0bd7-4224-ac24-abacd1acefa4" />

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

 <img width="769" height="286" alt="image" src="https://github.com/user-attachments/assets/900c912b-637d-43ac-b5ac-3dfde97b7591" />

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
## OUTPUT
<img width="775" height="290" alt="image" src="https://github.com/user-attachments/assets/b2adb0b5-371a-435b-a004-c9bf832da668" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
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

<img width="775" height="290" alt="image" src="https://github.com/user-attachments/assets/d3b019b7-dc29-413b-8e37-a8aaf8ee03b0" />

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
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


<img width="586" height="183" alt="image" src="https://github.com/user-attachments/assets/e843e8c2-55a8-4d88-8bba-b4723eea9869" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="642" height="142" alt="image" src="https://github.com/user-attachments/assets/6ded40dc-047c-43c0-b42f-510d4e466c06" />


$ ./exread1.sh 
 
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


<img width="457" height="22" alt="image" src="https://github.com/user-attachments/assets/03b0dce6-e2a5-4dfc-bada-9ba253b0df79" />

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```

<img width="226" height="57" alt="image" src="https://github.com/user-attachments/assets/bdc27e88-843b-4e2b-8328-05d12785523a" />


$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
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

<img width="191" height="69" alt="image" src="https://github.com/user-attachments/assets/70349e36-5036-4770-88b7-dbf3113d07f0" />

$ ./argshift.sh 1 2 3
 
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
<img width="660" height="369" alt="image" src="https://github.com/user-attachments/assets/da592fb0-2b5d-4d9c-89a7-cba0cb00d4c8" />

 ./argshift.sh 1 2 3
 
 
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
<img width="457" height="245" alt="image" src="https://github.com/user-attachments/assets/2087aa48-f038-464e-9632-749834088e0e" />
 
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

<img width="682" height="371" alt="image" src="https://github.com/user-attachments/assets/ca0f2ae9-613c-4f89-840b-867c9e3f51ae" />

# RESULT:
The Commands are executed successfully.
