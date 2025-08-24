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

![os 1](https://github.com/user-attachments/assets/45f9d6ef-3d1e-4348-be3a-061f38c1dafe)


cat < file2
## OUTPUT

![os 2](https://github.com/user-attachments/assets/232e347b-b4b6-400d-a05d-ab85b5e5c693)
# Comparing Files
cmp file1 file2
## OUTPUT
 ![os 3](https://github.com/user-attachments/assets/88c1d3e6-0a43-482c-9ff2-5890767b8652) 
comm file1 file2
 ## OUTPUT
 ![os 4](https://github.com/user-attachments/assets/35716beb-c8d8-4d75-8d34-60d856d63f3c)
 
diff file1 file2
## OUTPUT
![os 5](https://github.com/user-attachments/assets/9970ea73-fc15-44a8-a969-5c2c031b8793)

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


![108](https://github.com/user-attachments/assets/abb0126d-ff51-4b8d-b43b-41e34004d641)


cut -d "|" -f 1 file22
## OUTPUT

![109](https://github.com/user-attachments/assets/5262fe5b-b4ec-4cea-baee-dafcd0704c3c)

cut -d "|" -f 2 file22
## OUTPUT
![110](https://github.com/user-attachments/assets/0b740037-c311-457c-81fe-1edd0162d044)


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

![os 10](https://github.com/user-attachments/assets/34cf08a0-7db2-452b-b0ec-1390988ee03a)

grep hello newfile 
## OUTPUT


![new10](https://github.com/user-attachments/assets/42acbfd3-c96d-4cda-9487-bf0660c9bc17)

grep -v hello newfile 
## OUTPUT
![os 11](https://github.com/user-attachments/assets/dae8694b-3ef2-488b-b1b2-cbe7c1936766)



cat newfile | grep -i "hello"
## OUTPUT


![os 12](https://github.com/user-attachments/assets/97a911b6-45e3-4341-922b-2336fe8c0b16)

cat newfile | grep -i -c "hello"
## OUTPUT

![os 13](https://github.com/user-attachments/assets/895a2cbf-245d-4428-a18f-6f126b5e822f)


grep -R ubuntu /etc
## OUTPUT
![os 15](https://github.com/user-attachments/assets/7364d855-2af0-4de7-96bc-4b084822f558)



grep -w -n world newfile   
## OUTPUT
![os 16](https://github.com/user-attachments/assets/f6effec6-f633-46f8-b1af-2d89c44c7a6e)


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
![111](https://github.com/user-attachments/assets/82f0feff-b931-465d-9103-fa674471d649)


egrep -w '(H|h)ello' newfile 
## OUTPUT


![112](https://github.com/user-attachments/assets/c49060ad-2434-4d93-9e2f-a0f44d0c5ba3)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![os 19](https://github.com/user-attachments/assets/3db4ccc9-5b43-4421-b589-eeab09b55316)


egrep '(^hello)' newfile 
## OUTPUT
![os 20](https://github.com/user-attachments/assets/5abaac36-2cdf-4e09-bdf0-7e1045664178)


egrep '(world$)' newfile 
## OUTPUT

![os 21](https://github.com/user-attachments/assets/c5a72da4-5da9-43c6-a33b-d871c98229d1)

egrep '(World$)' newfile 
## OUTPUT

![os 21](https://github.com/user-attachments/assets/efe0a60f-a693-4bde-9a10-a5217a73aa8a)
egrep '((W|w)orld$)' newfile 
## OUTPUT

![os 22](https://github.com/user-attachments/assets/3f787dd4-ea09-42af-ad93-d4b942d821db)


egrep '[1-9]' newfile 
## OUTPUT

![os 23](https://github.com/user-attachments/assets/dc72ec85-f3d6-4484-a729-f3cb793c3f85)

egrep 'Linux.*world' newfile 
## OUTPUT

![os 24](https://github.com/user-attachments/assets/c7fcf8d3-7612-42cf-8c61-6377920724de)

egrep 'Linux.*World' newfile 
## OUTPUT

![os 25](https://github.com/user-attachments/assets/a3f0394b-85f0-4369-8b92-f17ebef2e839)

egrep l{2} newfile
## OUTPUT

![os 26](https://github.com/user-attachments/assets/c6742da6-503b-460e-8bb8-a8187338e936)

egrep 's{1,2}' newfile
## OUTPUT 

![os 28](https://github.com/user-attachments/assets/6d8efd65-fe73-439a-9ef7-8db01b598303)


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

![os 32](https://github.com/user-attachments/assets/82b2f494-67a0-4c06-9a44-36be83fd88ca)

sed -n -e '$p' file23
## OUTPUT

![os 33](https://github.com/user-attachments/assets/1b521880-6181-45ea-b386-07ddf3d094ec)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![os 34](https://github.com/user-attachments/assets/70cb6541-6d05-49f3-aa23-4349a0d74a35)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![os 35](https://github.com/user-attachments/assets/3d5cc653-8bb2-44bb-acbd-9f03d8dbd26f)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![os 36](https://github.com/user-attachments/assets/7ec97fa3-94ab-4d8c-95dc-0c84a614555c)

sed -n -e '1,5p' file23
## OUTPUT

![os 37](https://github.com/user-attachments/assets/26bf76d2-4cb9-402e-8bbf-9411462f9116)

sed -n -e '2,/Joe/p' file23
## OUTPUT

![os 38](https://github.com/user-attachments/assets/489aecf1-c7c8-42cc-9789-88b0725bfa33)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![os 39](https://github.com/user-attachments/assets/bb1e1abc-cb3c-4bda-b9e3-ba476109a603)

seq 10 
## OUTPUT

![os 40](https://github.com/user-attachments/assets/716076b0-624c-4280-aae5-fc7e7eba6516)

seq 10 | sed -n '4,6p'
## OUTPUT
![os 41](https://github.com/user-attachments/assets/7e64642c-f2b7-4d25-ba95-1fc9afb1d005)


seq 10 | sed -n '2,~4p'
## OUTPUT

![os 42](https://github.com/user-attachments/assets/bd7f9a29-002f-431f-a964-cb86cc49c73c)

seq 3 | sed '2a hello'
## OUTPUT

![os 43](https://github.com/user-attachments/assets/841325fe-5a3e-475e-b467-116be20ca3ef)

seq 2 | sed '2i hello'
## OUTPUT

![os 44](https://github.com/user-attachments/assets/7b3e6d82-e59f-49eb-9ef5-40eb79c991bf)
seq 10 | sed '2,9c hello'
## OUTPUT

![os 45](https://github.com/user-attachments/assets/3db7a343-e554-44f6-a852-19448535d5e1)
sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![os 46](https://github.com/user-attachments/assets/4b741865-61b0-41fd-adef-c0c629c4719b)


sed -n '2,4{s/$/*/;p}' file23


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
![os 49](https://github.com/user-attachments/assets/d6d3d497-329c-4e4f-b614-a2df1eaed832)


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

![113](https://github.com/user-attachments/assets/302fe84a-9ea6-4c33-b8d1-ed3257963d63)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![os 51](https://github.com/user-attachments/assets/0d836af6-dda2-40f0-8f2d-1fa4186efe95)
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

![os 53](https://github.com/user-attachments/assets/adbb939c-3dbe-4b8a-ab87-56821d64c5bc)
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![os 54](https://github.com/user-attachments/assets/91827cc4-179b-4c99-a647-2dec382268cc)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![100](https://github.com/user-attachments/assets/be92064c-be65-457e-97b4-f5cff5420cd7)

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![101](https://github.com/user-attachments/assets/52b55174-b9ed-4cfe-80a6-f351d602e32b)


tar -xvf backup.tar
## OUTPUT
![103](https://github.com/user-attachments/assets/cb74dff7-2dd9-4046-8eae-bbd33b1368bb)
gzip backup.tar

ls .gz
## OUTPUT
  ![114](https://github.com/user-attachments/assets/31401447-2616-4c35-93ea-5105f7ae6e8d)

gunzip backup.tar.gz
## OUTPUT

 ![115](https://github.com/user-attachments/assets/e2068e35-52e4-48ae-937a-785b9646077a)
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

![117](https://github.com/user-attachments/assets/232a9582-c956-4fb1-886d-a4138e2f0c60)
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
![os 60](https://github.com/user-attachments/assets/f54387be-ae91-4091-85db-c8823549896c)
 
ls file1
## OUTPUT
![os 61](https://github.com/user-attachments/assets/346dd54e-8972-42fc-903f-8646c26c8d45)
echo $?
## OUTPUT 
![119](https://github.com/user-attachments/assets/75a066f4-1ea8-4e42-a505-13e43a3f4342)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![119](https://github.com/user-attachments/assets/3328be0f-fc24-4754-b8e3-f946ac3bc998)
abcd
 
echo $?
 ## OUTPUT

![120](https://github.com/user-attachments/assets/8ae83e0b-14bd-498d-8db0-307d0cce1989)

 
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

![70](https://github.com/user-attachments/assets/aa8e9c4d-d1cb-42c8-bbff-056290512781)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![71](https://github.com/user-attachments/assets/451f4430-8670-4976-91bb-b536a332cdf5)
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
![74](https://github.com/user-attachments/assets/f923be78-4a05-41c9-bc8f-6229c1b28552)

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
![76](https://github.com/user-attachments/assets/3a67de23-9c27-4b6d-867e-0fd98ce5c560)

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
![77](https://github.com/user-attachments/assets/5b9123f1-0189-4b4c-9bd7-82033fcbd6bd)

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
![78](https://github.com/user-attachments/assets/f16ff5e6-99ec-4018-8fe5-8ce166819d22)

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
![79](https://github.com/user-attachments/assets/575749e2-ee0d-4f3a-a56e-bdd6c25ad47e)

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
 ![80](https://github.com/user-attachments/assets/3b1a84f8-c462-4b21-929c-f5fdd6b3fe39)
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
  ![81](https://github.com/user-attachments/assets/cb475e02-3041-401a-b77f-2b47296ddfe9)
 
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
 
  ![82](https://github.com/user-attachments/assets/113aa492-226c-4b76-9c81-3d69c0c63d48)
 
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
 
 ![83](https://github.com/user-attachments/assets/80989f79-7844-46a3-911b-04ba52c7a80e)
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
 ![85](https://github.com/user-attachments/assets/9d3073b6-487a-411e-94c0-2cb2ec796872)
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
![107](https://github.com/user-attachments/assets/e2e19361-d84b-4a73-993f-db698d1ba284)

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
![86](https://github.com/user-attachments/assets/727711d1-0a65-4d96-8c7d-fcd6602bf4ff)

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
![87](https://github.com/user-attachments/assets/2c8df81c-20c7-4d90-8cd5-96fdbc41c30f)
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
![88](https://github.com/user-attachments/assets/3c7afd98-814a-44a6-90df-ac5910930f05)
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

 ![89](https://github.com/user-attachments/assets/e8c3b026-bc63-48ba-b05c-a21d9df8fe36)
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
![92](https://github.com/user-attachments/assets/55804715-3b2e-47fd-aad7-b5f2468d0382)
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

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
  ![93](https://github.com/user-attachments/assets/83030502-0f28-4513-957c-9d3303e08a6b)
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
![94](https://github.com/user-attachments/assets/124be7dd-de53-4518-8ea9-974805095cbd)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![95](https://github.com/user-attachments/assets/a55c5e85-5f8d-41b3-adfb-a5ccd637633b)

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
 ./funcex.sh 

 ![96](https://github.com/user-attachments/assets/f99fc5f1-dfcd-4eef-9881-c2cc9a4801ea)
 ./funcex.sh 1 2

 ![97](https://github.com/user-attachments/assets/37a05eaa-1a84-4170-a8c9-5eb9266bcf98)
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
  ![98](https://github.com/user-attachments/assets/6da6f3ee-12e6-4b8b-aa3c-398b21c8026a)
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
  ![98](https://github.com/user-attachments/assets/6da6f3ee-12e6-4b8b-aa3c-398b21c8026a)
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
![99](https://github.com/user-attachments/assets/7923915e-ba4b-48a4-90b1-c8e1abc72972)
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
  ![105](https://github.com/user-attachments/assets/1ffeb4cf-82c1-48f8-bb67-65740754c4c7)
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

![106](https://github.com/user-attachments/assets/61385812-8e6a-4a75-ac7c-166963bd056a)
# RESULT:
The Commands are executed successfully.
