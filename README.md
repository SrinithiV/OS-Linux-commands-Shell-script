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
![image](https://github.com/SrinithiV/OS-Linux-commands-Shell-script/assets/118722030/8ad87c41-5f54-496f-862f-fe15e2a20b93)

cat < file2
## OUTPUT
![image](https://github.com/SrinithiV/OS-Linux-commands-Shell-script/assets/118722030/6edf7aac-9cbd-4f87-a9fb-63ce0da13184)

# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/SrinithiV/OS-Linux-commands-Shell-script/assets/118722030/d8dd344e-b43c-4cb8-aae8-3a54b496182f)
 
comm file1 file2
 ## OUTPUT
![image](https://github.com/SrinithiV/OS-Linux-commands-Shell-script/assets/118722030/2052b10c-266d-4df4-baea-29898f6ebfb9)

diff file1 file2
## OUTPUT
![image](https://github.com/SrinithiV/OS-Linux-commands-Shell-script/assets/118722030/733b9761-595a-4040-be59-c42cbb12dc27)

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
![image](https://github.com/SrinithiV/OS-Linux-commands-Shell-script/assets/118722030/ff5705fa-abd5-4988-b132-21ad4eaf1297)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/SrinithiV/OS-Linux-commands-Shell-script/assets/118722030/81b9a967-f237-4363-9ed0-d8622e31844a)

cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/SrinithiV/OS-Linux-commands-Shell-script/assets/118722030/34344d0a-29e1-48ac-9811-f253716e3668)

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep hello newfile 
## OUTPUT
![Screenshot from 2024-03-23 23-54-15](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/63724b93-fcca-4938-a404-bd9b4995b2b1)

grep -v hello newfile 
## OUTPUT
![Screenshot from 2024-03-23 23-54-37](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/589f0abd-af32-439a-8849-9eef7f016cc4)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2024-03-23 23-55-19](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/c99f6d61-5936-4172-9d37-0a6f2ad30a83)


cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2024-03-23 23-55-53](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/c72a6466-2485-404a-815d-54a11649db09)


grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2024-03-23 23-56-30](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/1219a8bf-fb1a-442a-88af-8ce100faddb2)

grep -w -n world newfile   
## OUTPUT
![Screenshot from 2024-03-23 23-57-11](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/c7a7b1b2-3eec-4e23-8022-d8d1b4cfc6ac)

cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat < newfile
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
![Screenshot from 2024-03-24 00-10-39](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/d9e26297-e3dc-45f3-9073-e569383dcb5c)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2024-03-24 00-10-58](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/9f9b389b-d5d3-499d-9b6e-51185da37233)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2024-03-24 00-11-16](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/14d86bf5-a1fd-4041-ab10-35252dc7e7b5)

egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2024-03-24 00-11-35](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/9f68780b-12cb-4e61-90de-500447cd7744)

egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-03-24 00-11-52](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/a99cab3a-c99f-4ec2-aed2-7335c54b8e96)

egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-03-24 00-12-12](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/d1cd9cf9-7a61-4eb2-aeb5-7c8d2056ad5a)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2024-03-24 00-12-43](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/5276256d-9d65-4585-a028-91017058dd60)

egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-03-24 00-13-15](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/647b941f-ba7d-4bb7-bf08-b5318e645a48)

egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-03-24 00-16-22](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/ed845404-aa73-4785-b411-44180e829c7b)

egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-03-24 00-16-39](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/9e99ea52-6a0a-4cff-ba31-ee6fb2c21670)

egrep l{2} newfile
## OUTPUT
![Screenshot from 2024-03-24 00-17-15](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/a41f58df-29ca-402f-b96b-b5af1676b532)

egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-03-24 00-17-34](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/180418de-210b-42b9-bee0-20d358c92238)

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
![Screenshot from 2024-03-24 00-25-05](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/766bb788-5a8e-466a-a045-74456d20c7d1)


sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2024-03-24 00-30-31](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/4e07a611-1907-465f-9539-184c68b993ad)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-03-24 00-30-51](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/250ebe77-fb02-45df-97fc-02b2b9b7b727)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-03-24 00-31-22](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/162348ee-41aa-4670-a507-83982e7d711f)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-03-24 00-31-41](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/e832aac3-2385-4cf3-9392-302efad8179e)


sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2024-03-24 00-32-01](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/7d9dcaab-c23b-452a-b67b-804e5f790090)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-03-24 00-32-40](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/51ede161-e9ec-45cd-a9bc-2fc69477cea7)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-03-24 00-33-07](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/631f527d-5cdc-414a-9fd2-5435172a98bb)


seq 10 
## OUTPUT
![Screenshot from 2024-03-24 00-40-16](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/4d440763-5fd3-45d0-816d-b5f797e11f69)


seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2024-03-24 00-40-40](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/54f326b2-5cb7-4ebe-be2f-9306a05a8da5)


seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2024-03-24 00-41-06](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/a5103deb-3497-4267-b45d-ed004de79b99)

seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2024-03-24 00-41-20](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/82482a58-e8d6-46b5-baae-4aa605017c57)

seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-03-24 00-41-42](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/a97aef8a-276f-45af-adc5-2f40d199729d)

seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2024-03-24 00-42-15](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/f976d0f4-c39e-4bef-a037-2f57c85ad9e1)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2024-03-24 00-43-02](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/f526b458-d3e2-4059-a178-a5bc84fc155d)

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot from 2024-03-24 00-43-33](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/1a1cd471-eb48-4ebd-a1bb-68bea6433dfa)

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
![Screenshot from 2024-03-24 00-56-25](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/39a9a5a0-6d8b-47b5-81e8-17c339c9ba00)


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
![Screenshot from 2024-03-24 00-57-02](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/c492ffdf-60a6-405b-b5c2-af53e8c57c54)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-03-24 00-57-35](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/bfc897f6-0dba-40c6-91cf-3d36c34e8447)

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![Screenshot from 2024-03-24 01-06-40](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/199038af-1ef0-43e7-bd83-df8105a78e59)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2024-03-24 01-07-16](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/ab2c2d3f-5edf-47d6-8cc9-392d90365175)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2024-03-24 01-48-37](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/dd8831a5-ab50-4ff3-9446-8104632d61c3)


mkdir backupdir
 
mv backup.tar backupdir
## OUTPUT
![Screenshot from 2024-03-24 01-49-07](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/5b2c19d1-491f-4fa0-9009-14e30c6c0ba9)

tar -tvf backup.tar
## OUTPUT
![Screenshot from 2024-03-24 01-50-13](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/97c3c2c5-057f-41aa-97e4-f00baa4beee6)

tar -xvf backup.tar
## OUTPUT
![Screenshot from 2024-03-24 01-50-42](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/58990426-6a00-4586-9c98-c3c2585ae7f1)

gzip backup.tar
ls .gz
## OUTPUT
 ![Screenshot from 2024-03-24 01-51-23](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/d8837a17-0412-4668-a95f-d898853202ef)

gunzip backup.tar.gz
## OUTPUT
![Screenshot from 2024-03-24 01-51-59](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/e0734906-f188-4531-83b5-14996f6cefd0)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![Screenshot from 2024-03-24 01-59-32](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/abca90db-d332-4495-a413-a9a244d329e3)

![Screenshot from 2024-03-24 02-12-58](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/c31f4062-7ff1-4dfe-a438-60d618ee792f)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2024-03-24 02-16-54](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/28a50a1b-ab57-444c-844f-33d935e03098)

cat > scriptest.sh 
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
![Screenshot from 2024-03-24 14-10-30](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/6f7e0d55-e283-497b-9ffc-9346ef1c7594)

![Screenshot from 2024-03-24 14-10-11](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/5d306f09-a162-45f5-9ee1-771b5972176c)

ls file1
## OUTPUT
![Screenshot from 2024-03-24 02-35-46](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/a50f7442-079f-448d-a4ed-b716878a42f8)

echo $?
## OUTPUT
![Screenshot from 2024-03-24 02-36-01](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/0043a1f1-db91-4fc3-b61e-841ab089880c)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![Screenshot from 2024-03-24 02-37-07](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/0b1e404d-6290-4287-bb8c-d65161b851b9)

abcd
 
echo $?
 ## OUTPUT
 
![Screenshot from 2024-03-24 02-36-01](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/0043a1f1-db91-4fc3-b61e-841ab089880c)

 
# mis-using string comparisons

cat > strcomp.sh 
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

![Screenshot from 2024-03-24 09-55-07](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/a42b3b5b-ac9c-42fd-8086-f2c823ba71a8)

chmod 755 strcomp.sh
 
./strcomp.sh 

## OUTPUT

![Screenshot from 2024-03-24 02-50-32](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/39ae40f1-4a27-4271-894b-f9c46cfef779)

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

![Screenshot from 2024-03-24 14-16-58](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/5beba1df-fa57-4942-ab19-2564855f96d7)

![Screenshot from 2024-03-24 14-17-16](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/a12ea18e-828c-4987-8d50-b68f670acbd1)

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

![Screenshot from 2024-03-24 10-39-51](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/f5169305-52cb-4142-8753-8c7625cdbc37)

![Screenshot from 2024-03-24 10-39-10](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/3d25f5f1-9574-4a20-8899-096136d6a859)

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

![Screenshot from 2024-03-24 10-37-08](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/5a8edb24-6f06-45ad-8173-54d193955472)

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

![Screenshot from 2024-03-24 10-39-51](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/f5169305-52cb-4142-8753-8c7625cdbc37)

![Screenshot from 2024-03-24 10-38-27](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/05c26e6f-0068-458d-bad5-55719be33d16)

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
![Screenshot from 2024-03-24 10-56-26](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/6fe1a64c-31c8-4289-955c-c7aa9d1fb802)

![Screenshot from 2024-03-24 10-57-18](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/9be00cae-6d47-42cd-8748-63a3f0042f5e)

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
![Screenshot from 2024-03-24 11-03-40](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/e57793cc-0e08-4554-96da-0029b53f3c38)

![Screenshot from 2024-03-24 11-00-32](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/f274fa34-fe0d-4bd8-863e-f9f0c255c562)

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
## OUTPUT
![Screenshot from 2024-03-24 11-07-59](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/f396cfe4-d702-48c2-9999-09e9a5ff297e)

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
![Screenshot from 2024-03-24 11-12-18](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/d1dbb9ce-33d0-408f-a8f9-1c8c2c415a1b)

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

![Screenshot from 2024-03-24 11-14-52](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/c85c3b39-46ff-46fa-a0ff-2c7ca263dcc8)

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

![Screenshot from 2024-03-24 11-21-54](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/2a640093-0981-47ca-97cb-e8f6cd1951cc)
 
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

## OUTPUT

![Screenshot from 2024-03-24 11-28-13](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/c4fffd22-9616-47fb-96a2-fe68789de102)

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

![Screenshot from 2024-03-24 11-55-51](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/90ad1598-ecde-49e1-94e9-2f5ef073d8dd)

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
![Screenshot from 2024-03-24 12-18-54](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/960ac2dd-aa74-4072-9df5-75756c7fefd2)

![Screenshot from 2024-03-24 12-19-11](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/ab11857a-a1f9-422d-ae92-7d4f33a1c238)

![Screenshot from 2024-03-24 12-19-41](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/9cd218a9-1592-4f86-8e1c-23b6e61658c6)

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

![Screenshot from 2024-03-24 12-26-06](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/78606a49-27d0-4be4-98c9-b4e2eef694df)

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

![Screenshot from 2024-03-24 12-28-39](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/183e35c9-5afd-41a5-9777-ea0922aeaa29)
 
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

![Screenshot from 2024-03-24 12-30-35](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/c045080e-ca55-43cd-865b-7c9a6ad911de)

$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 

## OUTPUT

![Screenshot from 2024-03-24 12-32-56](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/034ef690-a54b-4018-b887-87ed06287376)

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

![Screenshot from 2024-03-24 12-34-58](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/5435ed19-b63f-4829-92fb-936eda53df30)

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

![Screenshot from 2024-03-24 12-39-16](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/9ee8108b-b64c-4b92-a19f-c991de0007ef)

 
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

./funcex.sh 1 2


## OUTPUT

![Screenshot from 2024-03-24 12-44-59](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/09bf33e1-25b6-49f9-bb00-83c5f4014380)

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

![Screenshot from 2024-03-24 12-47-22](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/ea51bab4-835c-4c75-adf8-29c804715153)

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
$ chmod 777 argshift1.sh

$ ./argshift1.sh 1 2 3

## OUTPUT

![Screenshot from 2024-03-24 12-49-47](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/ef0d8f6a-b9d5-4f8a-96f5-bcf0494d288f)

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

![Screenshot from 2024-03-24 12-55-57](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/6f26bffd-05d7-4b09-9082-fe6e91461c23)

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

![Screenshot from 2024-03-24 13-03-49](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/1e72a2f0-4353-4991-832d-2fcf10cd8eed)

![Screenshot from 2024-03-24 13-05-01](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/f588b1de-18ed-420d-be5d-0321dc2d052c)

![Screenshot from 2024-03-24 13-04-27](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/cd702a94-2a06-41b9-ad52-2ff131868a5e)

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

![Screenshot from 2024-03-24 14-27-27](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/c8df77a1-7f11-40c7-aba0-bb48474ed3c7)

![Screenshot from 2024-03-24 14-27-43](https://github.com/DHARINIPV/OS-Linux-commands-Shell-script/assets/119400845/781bc603-9133-4a49-b200-045d9d74fff4)

# RESULT:
The Commands are executed successfully.
