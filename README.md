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

<img width="414" height="134" alt="Screenshot from 2026-07-29 10-23-31" src="https://github.com/user-attachments/assets/4b7cda8a-d90d-465c-abab-4d2be83d51de" />



cat < file2
## OUTPUT
<img width="510" height="139" alt="Screenshot from 2026-07-29 10-23-51" src="https://github.com/user-attachments/assets/ef6a28e8-b190-4f78-a950-ed78774d0d3e" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="673" height="58" alt="Screenshot from 2026-07-29 10-24-21" src="https://github.com/user-attachments/assets/c5f51d36-6250-447d-94dc-d78a02b388f7" />

comm file1 file2
 ## OUTPUT
<img width="625" height="195" alt="Screenshot from 2026-07-29 10-24-54" src="https://github.com/user-attachments/assets/26456379-1e48-491e-99fc-e7abc9b185b8" />

 
diff file1 file2
## OUTPUT
<img width="625" height="231" alt="Screenshot from 2026-07-29 10-25-16" src="https://github.com/user-attachments/assets/f712b909-545c-4a9f-a4b6-42f9add54aa1" />


#Filters
Deletes a node present at a specific position in the singly linked list.	

O(N)
	

O(1)
From End	

Eliminates the last node of the singly linked list.
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

<img width="495" height="82" alt="Screenshot from 2026-07-29 10-27-49" src="https://github.com/user-attachments/assets/90a8fe6b-12b7-4f2b-a9c0-974cd3c484ef" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="518" height="119" alt="Screenshot from 2026-07-29 10-28-14" src="https://github.com/user-attachments/assets/0e7953de-2b38-4dcc-8134-5d5109e5dd39" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="518" height="119" alt="Screenshot from 2026-07-29 10-28-40" src="https://github.com/user-attachments/assets/12256dcc-681b-4187-b60b-89c3af33c417" />

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

<img width="621" height="52" alt="Screenshot from 2026-07-29 10-29-45" src="https://github.com/user-attachments/assets/dfaf42cf-df9b-4efe-bbec-a037fb30f58d" />



grep hello newfile 
## OUTPUT


<img width="621" height="52" alt="Screenshot from 2026-07-29 10-30-06" src="https://github.com/user-attachments/assets/fbcfbbb8-b824-41f6-a058-70f9d3c1baf0" />


grep -v hello newfile 
## OUTPUT
<img width="621" height="52" alt="Screenshot from 2026-07-29 10-30-34" src="https://github.com/user-attachments/assets/9bc97a04-657d-42b6-9bc4-2926b4b3de43" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="618" height="80" alt="Screenshot from 2026-07-29 10-30-55" src="https://github.com/user-attachments/assets/9c41fc9c-4de2-47eb-b6c3-93409b7a17b6" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="620" height="52" alt="Screenshot from 2026-07-29 10-31-17" src="https://github.com/user-attachments/assets/904c1809-138d-42e1-a677-77dbad3cd7a5" />



grep -R ubuntu /etc
## OUTPUT
<img width="1920" height="1080" alt="Screenshot from 2026-07-29 10-31-59" src="https://github.com/user-attachments/assets/186c8da5-224b-4720-a152-dfb64b145afe" />



grep -w -n world newfile   
## OUTPUT
<img width="680" height="74" alt="Screenshot from 2026-07-29 10-32-59" src="https://github.com/user-attachments/assets/db835f5e-1298-4025-a93c-428debe3d044" />


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
<img width="628" height="78" alt="Screenshot from 2026-07-29 10-34-49" src="https://github.com/user-attachments/assets/7f89f05e-b54b-420b-8444-f1556de64913" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="628" height="78" alt="Screenshot from 2026-07-29 10-35-15" src="https://github.com/user-attachments/assets/875b1178-6fdf-44eb-b9da-d8098388a079" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="628" height="78" alt="Screenshot from 2026-07-29 10-35-53" src="https://github.com/user-attachments/assets/33a1c048-8fe0-49d3-84ff-20a3a559896c" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="610" height="63" alt="Screenshot from 2026-07-29 10-36-26" src="https://github.com/user-attachments/assets/fe7691fb-29d6-42e6-93bc-9751851cde33" />


egrep '(world$)' newfile 
## OUTPUT
<img width="615" height="76" alt="Screenshot from 2026-07-29 10-36-49" src="https://github.com/user-attachments/assets/9f4a178f-b01d-491f-8718-2e444845c97b" />



egrep '(World$)' newfile 
## OUTPUT
<img width="615" height="76" alt="Screenshot from 2026-07-29 10-37-08" src="https://github.com/user-attachments/assets/beb57e60-63da-447a-b056-1a04d222202f" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="616" height="108" alt="Screenshot from 2026-07-29 10-37-45" src="https://github.com/user-attachments/assets/d53a3711-1c8a-47b7-a53d-4e0ccbc7e8c8" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="609" height="66" alt="Screenshot from 2026-07-29 10-38-08" src="https://github.com/user-attachments/assets/09d0602b-2ba6-4a15-b235-bec8d7389f91" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="613" height="80" alt="Screenshot from 2026-07-29 10-38-37" src="https://github.com/user-attachments/assets/d57773da-4952-446a-9b26-77a2d8f66389" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="608" height="59" alt="Screenshot from 2026-07-29 10-39-11" src="https://github.com/user-attachments/assets/16d7e79a-c1d0-4b67-8b68-f8a543ee3929" />


egrep l{2} newfile
## OUTPUT

<img width="613" height="79" alt="Screenshot from 2026-07-29 10-39-32" src="https://github.com/user-attachments/assets/9a822a53-b5c0-41f6-811d-a68a262f8d4c" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="617" height="104" alt="Screenshot from 2026-07-29 10-39-54" src="https://github.com/user-attachments/assets/50f4fca3-60f3-4760-a687-aa44b2cf5aac" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |
  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

<img width="631" height="81" alt="Screenshot from 2026-07-29 10-42-28" src="https://github.com/user-attachments/assets/fcc42ba7-db80-46a7-8d42-7cf8e38a9c9b" />


sed -n -e '$p' file23
## OUTPUT
<img width="623" height="71" alt="Screenshot from 2026-07-29 10-43-00" src="https://github.com/user-attachments/assets/4de5f5fd-db67-4da5-aeea-a02e7868c1f6" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="692" height="237" alt="Screenshot from 2026-07-29 10-43-29" src="https://github.com/user-attachments/assets/a36bc96a-1cda-45c2-99f4-6ef43543b1f9" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="692" height="237" alt="Screenshot from 2026-07-29 10-43-52" src="https://github.com/user-attachments/assets/f8dd8425-c4f5-4a94-a298-38868e1fc72c" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="693" height="256" alt="Screenshot from 2026-07-29 10-44-19" src="https://github.com/user-attachments/assets/e64f9459-f736-464f-b84f-fb8257a6751e" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="693" height="154" alt="Screenshot from 2026-07-29 10-44-43" src="https://github.com/user-attachments/assets/d13523db-3fe5-4657-8ad7-5671e8391920" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="699" height="106" alt="Screenshot from 2026-07-29 10-45-03" src="https://github.com/user-attachments/assets/3fe7dcd1-2b67-4652-aff7-fd39af452bed" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="626" height="87" alt="Screenshot from 2026-07-29 10-47-11" src="https://github.com/user-attachments/assets/b391ff53-2a9c-4075-addc-091f164eeefa" />


seq 10 
## OUTPUT

<img width="638" height="262" alt="Screenshot from 2026-07-29 10-47-34" src="https://github.com/user-attachments/assets/1fa97266-a364-42bf-8f9e-984b8b5082e5" />




seq 10 | sed -n '4,6p'
## OUTPUT

<img width="628" height="125" alt="Screenshot from 2026-07-29 10-48-11" src="https://github.com/user-attachments/assets/d530c9f5-9aa3-44f8-857b-cdeef6035100" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="631" height="103" alt="Screenshot from 2026-07-29 10-48-32" src="https://github.com/user-attachments/assets/786104da-84d4-4756-8afc-f3540be877d7" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="638" height="125" alt="Screenshot from 2026-07-29 10-49-03" src="https://github.com/user-attachments/assets/28592275-39c4-4662-baf3-241bb870ff7e" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="634" height="106" alt="Screenshot from 2026-07-29 10-49-24" src="https://github.com/user-attachments/assets/ca8a6960-d5b4-447f-9ac0-18f19c3215ae" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="634" height="106" alt="Screenshot from 2026-07-29 10-49-49" src="https://github.com/user-attachments/assets/6c5cc861-4927-457c-8c91-339bf6824f44" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="634" height="106" alt="Screenshot from 2026-07-29 10-50-20" src="https://github.com/user-attachments/assets/119d3d7b-3def-4325-a6c4-0728dde25cf5" />



sed -n '2,4{s/$/*/;p}' file23

<img width="634" height="106" alt="Screenshot from 2026-07-29 10-50-20" src="https://github.com/user-attachments/assets/276216a9-3b09-4313-9d7c-4f4d99f87d14" />

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
<img width="655" height="155" alt="Screenshot from 2026-07-29 10-57-16" src="https://github.com/user-attachments/assets/66b00abf-d963-4a68-b9ed-a7f600803294" />


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

<img width="655" height="155" alt="Screenshot from 2026-07-29 10-58-42" src="https://github.com/user-attachments/assets/50c9672c-53bf-4177-b19e-ba626391df39" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="639" height="247" alt="Screenshot from 2026-07-29 11-00-04" src="https://github.com/user-attachments/assets/589650a4-1fb5-4fe1-9455-f1f167c8ed61" />

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
<img width="647" height="119" alt="Screenshot from 2026-07-29 11-01-03" src="https://github.com/user-attachments/assets/e1ba500c-bddc-4037-a428-a8def039edef" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="647" height="119" alt="Screenshot from 2026-07-29 11-01-23" src="https://github.com/user-attachments/assets/9b3cd9bc-c071-4046-945c-5cf1be4f6d1e" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="645" height="332" alt="Screenshot from 2026-07-29 11-01-56" src="https://github.com/user-attachments/assets/0d2211fe-5e84-4b41-901a-5224f4fe971b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="799" height="393" alt="Screenshot from 2026-07-29 11-04-27" src="https://github.com/user-attachments/assets/0520b5e2-c70d-4aa7-8f73-1039cf709a38" />



tar -xvf backup.tar
## OUTPUT
<img width="805" height="330" alt="Screenshot from 2026-07-29 11-05-52" src="https://github.com/user-attachments/assets/a7dcc62b-b636-4e97-a1b1-df54baf485c4" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="653" height="98" alt="Screenshot from 2026-07-29 13-54-24" src="https://github.com/user-attachments/assets/9117a9d3-b7c5-4713-97c1-9b61a3976402" />

gunzip backup.tar.gz
## OUTPUT
<img width="653" height="98" alt="Screenshot from 2026-07-29 13-55-12" src="https://github.com/user-attachments/assets/36d95102-ff97-4637-8b57-39d79857bda5" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="690" height="116" alt="Screenshot from 2026-07-29 14-24-02" src="https://github.com/user-attachments/assets/7ca858b0-78fb-4c97-af36-efe5fa8f0489" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
##OUTPUT

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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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

 
 ./funcex.sh 1 2

 
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


# RESULT:
The Commands are executed successfully.
