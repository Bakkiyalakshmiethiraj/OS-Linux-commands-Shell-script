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
![Screenshot 2024-03-21 112529](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/316e6f8f-437f-431f-bf66-3f07c642dbfb)

cat < file2
## OUTPUT
![Screenshot 2024-03-21 112315](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/75d17ae9-fcb7-46ca-9497-9ceea9e0e2bc)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2024-03-21 112432](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/d6bb210d-c803-40c9-b361-9c8bd081acb7)

comm file1 file2
 ## OUTPUT
![Screenshot 2024-03-21 112704](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/fd6da28b-36b0-4b7c-ae1b-da9f321a0cd6)

 
diff file1 file2
## OUTPUT

![Screenshot 2024-03-21 112747](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/ab8dfd60-e33f-4d41-9e81-38f763e2802e)

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
![Screenshot 2024-03-21 113301](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/2df9a16b-b8c9-491a-9caa-cf7f4c8c2875)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2024-03-21 113530](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/a66ef34b-4acd-4cbb-87eb-3b76b4daa7a1)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2024-03-21 113430](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/f53a0dd9-7d3b-4dcd-a338-e56f3db21a51)


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
![Screenshot 2024-03-21 113850](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/55225733-5b8a-4fa1-bae0-fd17cdc24772)



grep hello newfile 
## OUTPUT
![Screenshot 2024-03-21 113948](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/48e35e52-a859-43a5-b872-4e86f3e84f4e)




grep -v hello newfile 
## OUTPUT
![Screenshot 2024-03-21 114050](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/7c124834-5fbc-4206-9c1f-a435737b08d8)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot 2024-03-21 114149](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/c7379103-cdda-40ed-9e69-bde353e34a85)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot 2024-03-21 114255](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/f171dc3c-ad28-4b78-8ad8-79d58f3ce0f0)



grep -R ubuntu /etc
## OUTPUT
![Screenshot 2024-03-21 114452](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/dac4c8bc-df80-4513-bb24-3d5a8b3e1880)



grep -w -n world newfile   
## OUTPUT
![Screenshot 2024-03-21 114748](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/afa44085-25fd-4ab1-873f-cff108faccd6)


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
![Screenshot 2024-03-21 115341](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/5c17d654-786f-41d3-b20f-32fdf15e5d7c)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2024-03-21 115451](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/3588c168-94d9-4803-9313-aabf853bd894)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot 2024-03-21 115551](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/c2e0425a-9b7e-44ea-a39c-2f73293aa0d2)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2024-03-21 134800](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/8cda819f-1c93-4697-8a03-1e28ae83152b)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot 2024-03-21 135124](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/e514ec43-d482-423c-8e78-f88bd12ee249)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot 2024-03-21 135232](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/a704cf99-6417-4053-8584-c0f4b634a4b0)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2024-03-21 135339](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/bb2256e9-2c7e-469c-b76e-3497fb8688b9)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot 2024-03-21 135433](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/379d0126-32f2-4c4c-ac92-2f3d023f7d3f)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2024-03-21 135710](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/a69a5068-0480-4fa8-bfbb-f949087b34e2)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot 2024-03-21 135710](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/1f521f99-be90-47e9-9712-bd2a7a03ee8e)


egrep l{2} newfile
## OUTPUT
![Screenshot 2024-03-21 135844](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/13db49b8-0b2c-4620-889a-59b9c747b99e)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot 2024-03-21 140019](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/3bb03847-6ab2-4624-9b8e-02bff2ba02e9)


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
![Screenshot 2024-03-21 140557](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/7c821be5-9f47-4c9e-a6aa-3c4bf154b940)



sed -n -e '$p' file23
## OUTPUT
![Screenshot 2024-03-21 142427](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/39513c0f-5c38-46a2-bccc-fe11fddd076f)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2024-03-21 142556](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/53da0ee2-34e0-4a9d-bf17-2de754d3bd43)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot 2024-03-21 142725](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/aae2a877-c29a-4122-b285-5bbbfa22dd89)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2024-03-21 142841](https://github.com/Bakkiyalakshmiethiraj/OS-Linux-commands-Shell-script/assets/144870983/ce802bf0-9d20-4538-a6b2-bc779a68277f)



sed -n -e '1,5p' file23
## OUTPUT



sed -n -e '2,/Joe/p' file23
## OUTPUT




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT



seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT



seq 2 | sed '2i hello'
## OUTPUT


seq 10 | sed '2,9c hello'
## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



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
