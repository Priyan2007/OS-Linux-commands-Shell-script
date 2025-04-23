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
![Screenshot from 2025-03-05 10-39-17](https://github.com/user-attachments/assets/65f6e7ec-7970-4a4f-ad9f-ce205b989706)




cat < file2
## OUTPUT
![Screenshot from 2025-03-05 10-39-35](https://github.com/user-attachments/assets/9c345b4f-261e-4c9a-926d-fa0bc70b49f7)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-03-05 10-41-08](https://github.com/user-attachments/assets/511bf3cd-3f4d-40a4-a03b-beae4fca2874)


comm file1 file2
 ## OUTPUT
 ![Screenshot from 2025-03-05 10-41-30](https://github.com/user-attachments/assets/12f7bf46-3647-43f5-93e9-5b5eb1a37f73)


 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-05 10-41-45](https://github.com/user-attachments/assets/a83b5968-b67b-4858-9abc-a07dbd73690a)



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
![Screenshot from 2025-03-05 10-44-22](https://github.com/user-attachments/assets/e82a7377-5a51-4c6f-b4a7-13faa8fd960d)





cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-05 10-44-38](https://github.com/user-attachments/assets/8ec43151-7aba-49a7-95dc-a1d00b6705f0)




cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-05 10-44-49](https://github.com/user-attachments/assets/991b8f2b-ed1c-4632-b479-1b5828597e84)



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
![Screenshot from 2025-03-05 10-47-39](https://github.com/user-attachments/assets/56f3293d-2f49-4f81-ac02-5a798b7a7e34)




grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-05 10-47-51](https://github.com/user-attachments/assets/8eaef493-0be2-4550-9287-f3d5eadb7ce8)





grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-05 10-48-10](https://github.com/user-attachments/assets/03958186-a91f-4eaf-9d6c-cf21ec1a2715)




cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-03-05 10-48-37](https://github.com/user-attachments/assets/60c796f3-520a-4eb4-9d38-31538cb41bac)





cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-05 10-48-49](https://github.com/user-attachments/assets/cdcec856-946b-4ffd-bfee-4786f6256901)




grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-03-05 10-50-34](https://github.com/user-attachments/assets/c1a03299-9a44-4719-a72b-75102b75dea9)




grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-03-05 10-49-02](https://github.com/user-attachments/assets/5436db2f-27d6-4562-95d9-e4fa4bf9d002)



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
![Screenshot from 2025-03-03 11-17-21](https://github.com/user-attachments/assets/eb1b71f9-58d8-4fef-938a-b3115d1f85a3)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-03-03 11-18-36](https://github.com/user-attachments/assets/6592b8ec-3aaf-4da8-820f-cf798b1cc689)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-03-03 11-19-56](https://github.com/user-attachments/assets/059731d3-ab8e-4a98-8fbf-6d3c6599d27e)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 11-20-23](https://github.com/user-attachments/assets/59e2104b-d271-4e3e-aa6b-68e763663ad7)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 11-21-34](https://github.com/user-attachments/assets/c519e10c-90d3-4917-b608-8363547085a2)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 11-22-10](https://github.com/user-attachments/assets/efed1af5-516d-4bcf-a3ab-3492a708bf00)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-03-03 11-22-35](https://github.com/user-attachments/assets/6a3d824a-19cb-469f-9e30-4e1dcc4bbfb2)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-03-03 11-22-55](https://github.com/user-attachments/assets/ea09cc56-c041-44bc-a84c-9e8e72a72526)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-03-03 11-23-36](https://github.com/user-attachments/assets/f44af8d9-11ec-4691-b9d8-406f3e8ae16b)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-03-03 11-24-06](https://github.com/user-attachments/assets/d09a4fff-2882-4a0d-ac5c-2437de41dbf4)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-03-03 11-24-59](https://github.com/user-attachments/assets/84feb542-1400-4ce9-9466-2f08cb6a1b86)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-03 11-25-21](https://github.com/user-attachments/assets/1f77f09f-94b2-4633-a370-415e743030f3)


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
![Screenshot from 2025-03-03 11-34-55](https://github.com/user-attachments/assets/c2e82f19-c60a-4c3d-901d-18ecbc76662e)



sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-03-03 11-36-09](https://github.com/user-attachments/assets/ed4b659d-c3a8-465b-acb2-53518f26fd10)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-03 11-36-40](https://github.com/user-attachments/assets/686ee1f3-18b4-40b7-98b6-b9359b37fdd3)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-03-03 11-37-14](https://github.com/user-attachments/assets/5c3fdc63-52f0-4b77-8a03-a024ed4cbcf7)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-03-03 11-37-34](https://github.com/user-attachments/assets/25671cde-a26d-4443-aff4-244bf054e990)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-03-03 11-37-59](https://github.com/user-attachments/assets/60feb4a6-9d8e-4f8b-ba6b-259ff4807fc2)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-03 11-38-29](https://github.com/user-attachments/assets/fe259ffe-eb6b-4fd8-81a4-fd5aae151b85)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-03 11-40-40](https://github.com/user-attachments/assets/1d497618-f63b-40a9-bc22-141c0e4c6a4d)



seq 10 
## OUTPUT
![Screenshot from 2025-03-03 11-41-19](https://github.com/user-attachments/assets/860f121d-79cf-4130-ae88-ab9eb7541648)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-03-03 11-41-40](https://github.com/user-attachments/assets/c97fc4cc-a40a-411f-92d1-d80bcabc22a5)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-03-03 11-42-10](https://github.com/user-attachments/assets/d4834ac4-5c26-4e75-92a7-7a394711ec65)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-03-03 11-42-49](https://github.com/user-attachments/assets/c19a4330-be30-416c-863d-fababb4bf201)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-03-03 11-43-15](https://github.com/user-attachments/assets/792bdd1d-9f03-45ee-90f9-b12482734868)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-03-03 11-43-36](https://github.com/user-attachments/assets/b3500736-2a48-43ca-aa14-e7397e27886f)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-03-03 11-44-08](https://github.com/user-attachments/assets/b9a67070-a79b-411b-b707-c47d42a95d30)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot from 2025-03-03 11-44-31](https://github.com/user-attachments/assets/857ab7f1-c7b7-4324-a47c-ea2354a837f3)




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
![Screenshot from 2025-03-05 11-01-08](https://github.com/user-attachments/assets/205a9f3d-1f42-468f-9fb4-12f86ea3540b)


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
![Screenshot from 2025-03-05 11-01-19](https://github.com/user-attachments/assets/791bdc40-409c-441c-8ec0-9ca0561b1b45)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

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
![Screenshot from 2025-04-23 10-23-09](https://github.com/user-attachments/assets/c0ebdc98-7831-4fe0-827d-88952de245f9)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-04-23 10-23-42](https://github.com/user-attachments/assets/b3ed6dab-43d0-430c-9203-349895747779)



#Backup commands
tar -cvf backup.tar *
## OUTPUT![Screenshot from 2025-04-23 10-26-45](https://github.com/user-attachments/assets/f088c040-a1e1-40b0-bdbe-d282d94e3c98)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2025-04-23 10-30-39](https://github.com/user-attachments/assets/77197caf-d160-472d-aa0a-7fa2df4a185b)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2025-04-23 10-31-11](https://github.com/user-attachments/assets/ac46aa9e-b7ab-4ce2-834b-e46e68ef189c)

gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/user-attachments/assets/a1df8f02-49e0-4357-ac3c-aa8f43383e05)
gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/134e6655-9b8b-45fb-8a1e-ce4c9f07f4bb)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/98dba1e9-1cbe-4f70-83d1-8897562a91ee)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/2c42990b-fc7b-411f-8a38-334b5e691bac)

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
![image](https://github.com/user-attachments/assets/1a4b902c-d88b-403f-9b42-dbf075d70264)
 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/7ea4c54c-bacf-49ac-a433-694ba5c1b286)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/403f62bc-dfc9-4da3-b99b-0621acd17571)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/8b288ef9-fe00-41a9-8845-9e9730f26b29)

 
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
![image](https://github.com/user-attachments/assets/3df7ed21-c154-4cd3-89a6-285ead81b28b)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/1045ad7d-9745-4464-82e3-d76012b3e761)


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
![image](https://github.com/user-attachments/assets/4b930435-4abb-40cd-a088-f4cab02bad4c)


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
![image](https://github.com/user-attachments/assets/24322a45-c048-4a66-bd8d-ea749c611486)



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
![image](https://github.com/user-attachments/assets/b24eb56c-c19f-4e02-bc45-11f20f5cbede)


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
![image](https://github.com/user-attachments/assets/b01445b3-9206-4083-af24-4d1cfc2502d4)



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
![image](https://github.com/user-attachments/assets/cd1aa62a-067f-459c-81be-39919a9daa1a)


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
![image](https://github.com/user-attachments/assets/2a35a23e-6e64-4fc6-b959-f377b66acf25)


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
![image](https://github.com/user-attachments/assets/620b3c00-a8a5-4ccd-9989-b1b2fe27f4dd)

 
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
 ![image](https://github.com/user-attachments/assets/eb20e411-016f-4f6f-baef-16787a7d30f7)

 
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
 ![image](https://github.com/user-attachments/assets/ef4144dc-a5c2-46f1-b799-40cb12073d3e)

 
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
 ![image](https://github.com/user-attachments/assets/4e76d522-4f16-454a-954d-f796f775aaa3)

 
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

## OUTPUT
![image](https://github.com/user-attachments/assets/a6b24ec4-7bb2-4bde-a721-c597ef75f674)

 
cat forin3.sh 
```
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
```
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```


$ chmod 777 forinfile.sh

![image](https://github.com/user-attachments/assets/6e44d87a-137a-4d79-9cc2-6e7ef6011eaf)

```
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```

## OUTPUT
![image](https://github.com/user-attachments/assets/7934026f-f4b3-449f-91ee-247abb2eff01)



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
![image](https://github.com/user-attachments/assets/78654c91-5e21-4518-89c0-b1a3e2696fd5)



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
![image](https://github.com/user-attachments/assets/cc0f4d8d-faf2-4639-9394-481d65f8213f)



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
![image](https://github.com/user-attachments/assets/d08497a9-2281-4004-8b91-2de581c7c0b3)

 
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
![image](https://github.com/user-attachments/assets/dba1e608-c664-454e-bfbe-2eb9e1a01ec4)

 
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
![image](https://github.com/user-attachments/assets/39ac29cf-8e3b-4e71-bc7b-fb80c44561b9)


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

![image](https://github.com/user-attachments/assets/78d106b5-349f-41b9-be1c-7b423b660559)


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

![image](https://github.com/user-attachments/assets/6bbf25ff-deed-4b7a-9b0b-6337b956e486)


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

![image](https://github.com/user-attachments/assets/1838e628-eff1-489a-8332-f70bb34bf5fe)


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
 
![image](https://github.com/user-attachments/assets/22c0ccff-9fde-4e3a-a259-da97c8afbd71)

 
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
![image](https://github.com/user-attachments/assets/72da8202-017c-4613-88b0-d0aa3f4a390b)

 
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

![image](https://github.com/user-attachments/assets/1977daeb-d020-43ab-8768-4342aaf122fd)


# RESULT:
The Commands are executed successfully.
