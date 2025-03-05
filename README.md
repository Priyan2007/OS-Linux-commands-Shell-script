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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
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
