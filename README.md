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

![Screenshot 2024-08-28 081246](https://github.com/user-attachments/assets/1b2572e4-2a0a-413f-bdbb-fd5ed28f049a)



cat < file2
## OUTPUT

![Screenshot 2024-08-28 081301](https://github.com/user-attachments/assets/6f5632b0-863e-42e1-8123-bc805b2a04a1)


# Comparing Files
cmp file1 file2

![Screenshot 2024-08-28 081442](https://github.com/user-attachments/assets/9a7c7046-51d9-4231-980a-d6f914249a1e)

## OUTPUT
 
comm file1 file2
 ## OUTPUT
 
![Screenshot 2024-08-28 081516](https://github.com/user-attachments/assets/57c1dc74-5eea-4d24-8aef-332488a2f714)

 
diff file1 file2
## OUTPUT

![Screenshot 2024-08-28 081626](https://github.com/user-attachments/assets/a133d080-7122-4ec9-b435-3e5799514082)


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
![Screenshot 2024-08-28 081737](https://github.com/user-attachments/assets/1cd98c15-747b-40e3-838a-a87fb1994f8b)




cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2024-08-28 081747](https://github.com/user-attachments/assets/1be2b409-62a8-46b1-8374-8d9050ee0a23)



cut -d "|" -f 2 file22
## OUTPUT

![Screenshot 2024-08-28 081756](https://github.com/user-attachments/assets/5b85d8fa-0d4f-4b1d-92ca-ce811751572a)


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

![Screenshot 2024-08-28 081950](https://github.com/user-attachments/assets/1129095b-22ac-41b2-9617-4e184e4e7b39)



grep hello newfile 
## OUTPUT

![Screenshot 2024-08-28 082000](https://github.com/user-attachments/assets/513cc902-c03d-43c0-ae53-9bf5763c5d6d)




grep -v hello newfile 
## OUTPUT

![Screenshot 2024-08-28 082039](https://github.com/user-attachments/assets/a0090726-1b15-47ef-9111-100f14ae420e)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot 2024-08-28 082310](https://github.com/user-attachments/assets/02e81dc2-3262-405e-9e39-887b724e745a)




cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot 2024-08-28 082318](https://github.com/user-attachments/assets/c5be44d0-cca4-4714-a40b-6419a4e88391)




grep -R ubuntu /etc
## OUTPUT

![Screenshot 2024-08-28 082411](https://github.com/user-attachments/assets/89831286-a32e-4fdf-8304-7f15edda7908)



grep -w -n world newfile   
## OUTPUT

![Screenshot 2024-08-28 083446](https://github.com/user-attachments/assets/79867af7-13c9-41b4-806b-8ee51346c23b)


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

![Screenshot 2024-08-28 084511](https://github.com/user-attachments/assets/42b12730-a4e5-486c-870d-a189ed77018b)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2024-08-28 084528](https://github.com/user-attachments/assets/b08c4436-1f77-4c2a-aa80-09b029825b4d)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot 2024-08-28 084538](https://github.com/user-attachments/assets/f2358ee5-b225-43c8-a7d3-81ff95f481bd)



egrep '(^hello)' newfile 
## OUTPUT

![Screenshot 2024-08-28 084801](https://github.com/user-attachments/assets/39367db2-1fb0-4125-807b-2546f4c81558)



egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2024-08-28 084810](https://github.com/user-attachments/assets/7dfa2b63-2dc9-4582-8625-c4612921e79e)



egrep '(World$)' newfile 
## OUTPUT

![Screenshot 2024-08-28 084817](https://github.com/user-attachments/assets/50e5be33-ceea-4a9a-8dbb-826da827c4fb)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot 2024-08-28 084832](https://github.com/user-attachments/assets/562f8cbc-14cf-4937-bab1-8141a03df7df)



egrep '[1-9]' newfile 
## OUTPUT

![Screenshot 2024-08-28 084841](https://github.com/user-attachments/assets/457a3482-4439-4a65-b1d2-82e3307feade)



egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot 2024-08-28 084850](https://github.com/user-attachments/assets/1a6dff34-67d1-42ab-bef9-cf620a280355)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot 2024-08-28 084900](https://github.com/user-attachments/assets/db19c15d-140e-4dc2-913f-a93de67a72e0)


egrep l{2} newfile
## OUTPUT

![Screenshot 2024-08-28 084909](https://github.com/user-attachments/assets/fb7cf1e5-7564-451b-97f4-fcb16ad8255e)



egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot 2024-08-28 084916](https://github.com/user-attachments/assets/71f7f11a-fa5e-4c17-8fd9-a6335a707d8f)


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

![Screenshot 2024-08-28 085335](https://github.com/user-attachments/assets/60fc575b-47bf-4034-a047-a62ebe866707)



sed -n -e '$p' file23
## OUTPUT

![Screenshot 2024-08-28 085354](https://github.com/user-attachments/assets/f55e9f10-cec7-4dd2-97d8-18e6679124cb)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot 2024-08-28 085412](https://github.com/user-attachments/assets/8b4c6404-e13f-4d98-8ebb-faa8743a5c68)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot 2024-08-28 085734](https://github.com/user-attachments/assets/817bff5f-bbb8-4202-ac0e-25a8caf7634b)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot 2024-08-28 085748](https://github.com/user-attachments/assets/48ee0f7c-fad1-4446-b2fd-7df5d00f1461)



sed -n -e '1,5p' file23
## OUTPUT

![Screenshot 2024-08-28 085757](https://github.com/user-attachments/assets/6f2ec1c8-29ee-458b-aa6d-ef117c7cd7a9)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot 2024-08-28 085818](https://github.com/user-attachments/assets/e1483b3f-9c3a-4262-b88c-9df394c22641)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot 2024-08-28 085829](https://github.com/user-attachments/assets/ee649721-f00a-4942-a108-e7bd0736df7b)



seq 10 
## OUTPUT

![Screenshot 2024-08-28 085836](https://github.com/user-attachments/assets/7895cce1-f494-440a-bd69-9cea649bd168)



seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot2024-08-28 085844](https://github.com/user-attachments/assets/8bea6d49-f783-4e8e-b240-e6d14f2f7632)



seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot 2024-08-28 085900](https://github.com/user-attachments/assets/82dad090-d06d-4d68-8946-915ea2941304)



seq 3 | sed '2a hello'
## OUTPUT

![Screenshot 2024-08-28 090351](https://github.com/user-attachments/assets/a264d824-5ddd-47df-9d46-0c8f67d6b86a)



seq 2 | sed '2i hello'
## OUTPUT

![Screenshot 2024-08-28 090403](https://github.com/user-attachments/assets/0ff0cd50-4db1-45ec-997d-ccd9153ed127)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2024-08-28 090415](https://github.com/user-attachments/assets/c5a77b4f-ed51-47a6-a8b2-7a153c17bda4)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot 2024-08-28 090427](https://github.com/user-attachments/assets/61c35baf-f8f3-4c09-baea-1695f134a584)



sed -n '2,4{s/$/*/;p}' file23

![Screenshot 2024-08-28 090436](https://github.com/user-attachments/assets/c4f525be-a343-46c0-a432-b39bbb4067b8)


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

![Screenshot 2024-08-28 090514](https://github.com/user-attachments/assets/0981dd44-bbb4-4bec-aacb-1e7286547078)


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

![Screenshot 2024-08-28 090545](https://github.com/user-attachments/assets/4df76ae5-037c-49fd-8f9b-1045958ff053)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![Screenshot 2024-08-28 091127](https://github.com/user-attachments/assets/af9c8016-d10d-43c1-90f5-a7a0922cfd87)

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
 
![Screenshot 2024-08-28 145106](https://github.com/user-attachments/assets/04f5c9eb-c814-48f3-bd0e-185097927e21)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2024-08-28 145118](https://github.com/user-attachments/assets/823dc8e9-1faa-4152-bea7-c9cec355aa38)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot 2024-08-28 145149](https://github.com/user-attachments/assets/a6872df8-3ac5-47d6-8825-68279822efe3)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image-43](https://github.com/user-attachments/assets/28e14713-4dd5-494a-8b50-57b81f06561a)


tar -xvf backup.tar
## OUTPUT

gzip backup.tar
ls .gz
gunzip backup.tar.gz
## OUTPUT

![image-44](https://github.com/user-attachments/assets/5fe460c0-3c8d-494d-ba20-e9f4ad302c6d)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image-49](https://github.com/user-attachments/assets/3b17ce02-94f1-4ca9-bf74-89fc8779e08c)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image-50](https://github.com/user-attachments/assets/d72705f8-6c55-4286-9977-0226df8cd57f)


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

![image-51](https://github.com/user-attachments/assets/201f6b33-3522-49e6-a576-99f5711ecd1d)

 
ls file1
## OUTPUT

![image-52 (1)](https://github.com/user-attachments/assets/36250775-c499-4908-b218-4113db16ccbc)


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
![image-53](https://github.com/user-attachments/assets/2f7574ba-a8a8-4320-850b-976447f0730a)

## OUTPUT 

 ![image-53](https://github.com/user-attachments/assets/f3d8a394-1508-4bec-949a-6d5350cd7154)

abcd
 
echo $?
 ## OUTPUT

![image-54](https://github.com/user-attachments/assets/50444c52-c6c9-4ce7-a22f-a38f2e6476e3)

 
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

![image-55](https://github.com/user-attachments/assets/083f5a02-986d-4040-81e2-bbbb9ec7a296)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image-56](https://github.com/user-attachments/assets/a7b7d251-97aa-4a69-8607-2855fc756b1d)

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

![image-57](https://github.com/user-attachments/assets/69553499-1e69-41be-9aaf-e0058ce44ae6)

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

![image-58](https://github.com/user-attachments/assets/aa6de79a-8dea-4f10-a6df-370b16dd42b6)


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
![image-59](https://github.com/user-attachments/assets/bfb47d96-a745-4f42-9d70-26e6121eac13)


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

![image-60](https://github.com/user-attachments/assets/b4098a70-b7b7-4062-84f6-83d7b6995655)


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

![image-61](https://github.com/user-attachments/assets/3bbbc537-3cd4-473f-9f65-8135ac0ef2cc)


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

![image-62](https://github.com/user-attachments/assets/344799a1-fb0a-462b-8555-b1d97dd0b7b9)

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

 ![image-63](https://github.com/user-attachments/assets/63184387-5386-4cbf-81b8-174a26aa992a)

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

 ![image-64](https://github.com/user-attachments/assets/35efe8b3-b1f2-4f51-b6ad-4079f04a0a3e)

 
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
 
 ![image-65](https://github.com/user-attachments/assets/6072c32d-5c86-4903-b5a1-daee44591d34)

 
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

 ![image-66](https://github.com/user-attachments/assets/cc115b81-a498-46c0-a1d6-ddc11eeaa3d8)

 
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

 ![image-67](https://github.com/user-attachments/assets/66c2b729-37aa-4650-9c24-ca6902e6a3de)

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

 ![image-68](https://github.com/user-attachments/assets/675d2995-761b-4fe2-a63f-d8457c6fc924)

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

![image-69](https://github.com/user-attachments/assets/e25cc457-2248-4c8e-b332-358f698f992a)

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

![image-70](https://github.com/user-attachments/assets/14a320da-b577-495d-8ee1-b2b626e2ef4c)

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

![image-71](https://github.com/user-attachments/assets/6f0ee7bf-6f61-4566-b3f5-3845bfee1a18)

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
 
![image-72](https://github.com/user-attachments/assets/87e2e9f4-963d-4a67-80a7-6761a9534b92)

 
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

![image-73](https://github.com/user-attachments/assets/7ad544fe-4cdb-4a4b-a272-1b350517093c)

$ chmod 755 forbreak.sh


$ ./forbreak.sh 

  ![image-74](https://github.com/user-attachments/assets/3f861465-e421-429c-9f52-8997f0fd2b32)
  
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

 ![image-75](https://github.com/user-attachments/assets/758ae3bf-9551-402f-acab-4c51303497de)

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

![image-76](https://github.com/user-attachments/assets/c3b9b7e7-c5c8-4e5f-a878-76e2bf234da5)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image-77](https://github.com/user-attachments/assets/4fd61b15-6b14-4ef6-a44d-69ee33af8e4c)


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

![image-78](https://github.com/user-attachments/assets/4d91232c-816a-4cf6-aed8-11ba43e9b853)

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

![image-79](https://github.com/user-attachments/assets/8c3e6aca-fa2e-4601-a8e3-caee39e227a2)

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

![image-80](https://github.com/user-attachments/assets/2629528c-711f-42c2-99b4-37d35263c015)

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

![image-83](https://github.com/user-attachments/assets/c2176c02-494d-4c49-8966-d6bab077f7b5)

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

![image-82](https://github.com/user-attachments/assets/8be78200-22ae-4f32-9bfb-b1fa6522e488)

 
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

![image-84](https://github.com/user-attachments/assets/7458995f-948f-474a-b747-f7a594e2a14e)


# RESULT:
The Commands are executed successfully.
