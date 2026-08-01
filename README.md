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
<img width="555" height="432" alt="image" src="https://github.com/user-attachments/assets/7f5deed3-acaa-4faf-8f8e-4b73c75742d8" />



cat < file2
## OUTPUT
<img width="458" height="117" alt="Screenshot 2026-08-01 232633" src="https://github.com/user-attachments/assets/c57c8603-2ce6-4ccb-91bd-e1939a9d0e9e" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="457" height="90" alt="Screenshot 2026-08-01 232652" src="https://github.com/user-attachments/assets/181bf10d-1d19-4019-bf69-ae212fb9abe7" />

 
comm file1 file2
 ## OUTPUT

<img width="491" height="247" alt="Screenshot 2026-08-01 232720" src="https://github.com/user-attachments/assets/d4ab33b8-abf0-4312-9de4-eb6611219aac" />

 
diff file1 file2
## OUTPUT
<img width="432" height="242" alt="Screenshot 2026-08-01 232742" src="https://github.com/user-attachments/assets/31cad4c1-360d-47e7-804f-5268920de8a8" />


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

<img width="370" height="118" alt="Screenshot 2026-08-01 232802" src="https://github.com/user-attachments/assets/a0fe94e1-f96e-4406-81c5-b962bf567469" />





cut -d "|" -f 1 file22
## OUTPUT

<img width="423" height="146" alt="Screenshot 2026-08-01 233634" src="https://github.com/user-attachments/assets/cf735179-2f5e-43cc-aa16-8ba29e02ad8d" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="400" height="138" alt="Screenshot 2026-08-01 233732" src="https://github.com/user-attachments/assets/edd950cc-1c2d-4d1a-be01-b783dabb1f29" />

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

<img width="323" height="90" alt="Screenshot 2026-08-01 233750" src="https://github.com/user-attachments/assets/00c6d8bb-39b8-4c3c-8795-766991360e5d" />


grep hello newfile 
## OUTPUT
<img width="337" height="102" alt="Screenshot 2026-08-01 233807" src="https://github.com/user-attachments/assets/1f5da9fc-e804-45f1-884b-27a757e88c07" />




grep -v hello newfile 
## OUTPUT


<img width="366" height="92" alt="Screenshot 2026-08-01 233822" src="https://github.com/user-attachments/assets/42abd583-df80-41b3-ac37-5d98b204ba33" />



cat newfile | grep -i "hello"
## OUTPUT


<img width="453" height="117" alt="Screenshot 2026-08-01 233857" src="https://github.com/user-attachments/assets/55f09d8a-ee84-4501-a09b-91459ed0056b" />




cat newfile | grep -i -c "hello"
## OUTPUT


<img width="507" height="87" alt="Screenshot 2026-08-01 233911" src="https://github.com/user-attachments/assets/6d2ddf48-0c9b-4cf5-af2e-208068637feb" />



grep -R ubuntu /etc
## OUTPUT


<img width="815" height="642" alt="Screenshot 2026-08-01 233932" src="https://github.com/user-attachments/assets/ba56d4ce-1545-4c4d-aef9-314a21599113" />


grep -w -n world newfile   
## OUTPUT

<img width="412" height="117" alt="Screenshot 2026-08-01 234003" src="https://github.com/user-attachments/assets/1e6f8426-01dc-40fe-8465-7d7d64147adc" />


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

<img width="458" height="122" alt="Screenshot 2026-08-01 234020" src="https://github.com/user-attachments/assets/9c6ef5eb-67b5-448b-a3ba-db508f24265e" />



egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="440" height="120" alt="Screenshot 2026-08-01 234049" src="https://github.com/user-attachments/assets/f7724966-c027-457f-b584-c9107d37300a" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="478" height="117" alt="Screenshot 2026-08-01 234105" src="https://github.com/user-attachments/assets/1ebb3c03-867d-417f-9fa0-808b412fd72a" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="382" height="150" alt="Screenshot 2026-08-01 234121" src="https://github.com/user-attachments/assets/40ca1b74-9f09-45ae-b734-98a3270bd359" />


egrep '(world$)' newfile 
## OUTPUT


<img width="378" height="97" alt="Screenshot 2026-08-01 234136" src="https://github.com/user-attachments/assets/e4b0292a-f91e-489d-882b-6f7a2a43c9f4" />


egrep '(World$)' newfile 
## OUTPUT

<img width="382" height="95" alt="Screenshot 2026-08-01 234205" src="https://github.com/user-attachments/assets/05d242f3-9481-4c0b-8ba8-3285be31fe0e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="385" height="152" alt="Screenshot 2026-08-01 234220" src="https://github.com/user-attachments/assets/9baa334c-391a-46d0-a65e-83fc5cfe8363" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="373" height="87" alt="Screenshot 2026-08-01 234311" src="https://github.com/user-attachments/assets/ab0b71de-f915-4be7-aa81-35d5a408d725" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="376" height="85" alt="Screenshot 2026-08-01 234333" src="https://github.com/user-attachments/assets/5949501b-3a20-45e9-b128-33229d4bd801" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="376" height="85" alt="Screenshot 2026-08-01 234333" src="https://github.com/user-attachments/assets/5949501b-3a20-45e9-b128-33229d4bd801" />

egrep l{2} newfile
## OUTPUT


<img width="458" height="66" alt="Screenshot 2026-08-01 234400" src="https://github.com/user-attachments/assets/35605997-cddc-4afb-b170-9504d88fc0dd" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="366" height="167" alt="Screenshot 2026-08-01 234426" src="https://github.com/user-attachments/assets/2b499a4e-c20c-4023-8e71-506079038b36" />


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
<img width="418" height="62" alt="Screenshot 2026-08-01 234502" src="https://github.com/user-attachments/assets/5faaaa04-8713-4098-a81f-4fe5e4e7200f" />



sed -n -e '$p' file23
## OUTPUT
<img width="433" height="60" alt="Screenshot 2026-08-01 234516" src="https://github.com/user-attachments/assets/574ac933-631c-4452-907a-9dd4aadb7307" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="463" height="222" alt="Screenshot 2026-08-01 234532" src="https://github.com/user-attachments/assets/2b8c0ee0-bc34-4c6a-bf77-bac21b9f2d51" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="522" height="217" alt="Screenshot 2026-08-01 234553" src="https://github.com/user-attachments/assets/c6fb6db7-cbf6-4812-9103-dc7ea9c2fb26" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="643" height="335" alt="Screenshot 2026-08-01 234855" src="https://github.com/user-attachments/assets/9360ca2c-3c24-4a6c-b068-18425ec00917" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="643" height="222" alt="Screenshot 2026-08-01 235024" src="https://github.com/user-attachments/assets/ad46e85a-2bed-4cb8-a778-e2bc1a5eaf58" />


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

cd backupdir
 
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
