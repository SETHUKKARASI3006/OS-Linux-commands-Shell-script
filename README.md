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

![o1](/1.png)
<br>

cat < file2
## OUTPUT

![o2](/2.png)
<br>

# Comparing Files
cmp file1 file2
<br>

## OUTPUT

![o3](/3.png)
<br>
 
comm file1 file2
<br>

## OUTPUT

![o4](/4.png)
<br>
 
diff file1 file2
<br>

## OUTPUT

![o5](/5.png)
<br>

## Filters

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
<br>

## OUTPUT

![o6](/6.png)
<br>

cut -d "|" -f 1 file22
<br>

## OUTPUT

![o7](/7.png)
<br>

cut -d "|" -f 2 file22
<br>

## OUTPUT

![o8](/8.png)
<br>

cat < newfile 
```
Iam Sethukkarasi
iam Sethukkarasi
^d
```
```
cat > newfile 
Iam Sethukkarasi
iam Sethukkarasi
```
 
grep Iam newfile 
<br>

## OUTPUT

![o9](/9.png)
<br>

grep iam newfile 
<br>

## OUTPUT

![o10](/10.png)
<br>

grep -v iam newfile 
<br>

## OUTPUT

![o11](/11.png)
<br>

cat newfile | grep -i "iam"
<br>

## OUTPUT

![o12](/12.png)
<br>

cat newfile | grep -i -c "iam"
<br>

## OUTPUT

![o13](/13.png)
<br>

grep -R ubuntu /etc
<br>

## OUTPUT

![o14](/14.png)
<br>

grep -w -n Sethukkarasi newfile   
<br>

## OUTPUT

![o15](/15.png)
<br>

cat < newfile 
```
Iam Sethukkarasi
iam Sethukkarasi
I have 2 friends in college
I am from Artificial Intelligence & Data Science department
I am studying in Saveetha Engineering College
^d
```

cat > newfile
```
Iam Sethukkarasi
iam Sethukkarasi
I have 2 friends in college
I am from Artificial Intelligence & Data Science department
I am studying in Saveetha Engineering College
^d
 ```
egrep -w 'Iam|iam' newfile 
<br>

## OUTPUT

![o16](/16.png)
<br>

egrep -w '(I|i)am' newfile 
<br>

## OUTPUT

![o17](/17.png)
<br>

egrep -w '(I|i)a[a-z]' newfile 
<br>

## OUTPUT

![o18](/18.png)
<br>

egrep '(^iam)' newfile 
<br>

## OUTPUT

![o19](/19.png)
<br>

egrep '(college$)' newfile 
<br>

## OUTPUT

![o20](/20.png)
<br>

egrep '(College$)' newfile 
<br>

## OUTPUT

![o21](/21.png)
<br>

egrep '((C|c)ollege$)' newfile 
<br>

## OUTPUT

![o22](/22.png)
<br>

egrep '[1-9]' newfile 
<br>

## OUTPUT

![o23](/23.png)
<br>

egrep 'I.*college' newfile 
<br>

## OUTPUT

![o24](/24.png)
<br>

egrep 'I.*College' newfile 
<br>

## OUTPUT

![o25](/25.png)

egrep l{2} newfile
<br>

## OUTPUT

![o26](/26.png)
<br>

egrep 's{1,2}' newfile
<br>

## OUTPUT 

![o27](/27.png)

cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | Tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sid |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
<br>

## OUTPUT

![o28](/28.png)
<br>

sed -n -e '$p' file23
<br>

## OUTPUT

![o29](/29.png)
<br>

sed  -e 's/Ram/Sid/' file23
<br>

## OUTPUT

![o30](/30.png)
<br>

sed  -e '2s/Ram/Sid/' file23
<br>

## OUTPUT

![o31](/31.png)
<br>

sed  '/tom/s/5000/6000/' file23
<br>

## OUTPUT

![o32](/32.png)
<br>

sed -n -e '1,5p' file23
<br>

## OUTPUT

![o33](/33.png)
<br>

sed -n -e '2,/Joe/p' file23
<br>

## OUTPUT

![o34](/34.png)
<br>

sed -n -e '/Tom/,/Joe/p' file23
<br>

## OUTPUT

![o35](/35.png)
<br>

seq 10 
<br>

## OUTPUT

![o36](/36.png)
<br>

seq 10 | sed -n '4,6p'
<br>

## OUTPUT

![o37](/37.png)
<br>

seq 10 | sed -n '2,~4p'
<br>

## OUTPUT

![o38](/38.png)
<br>

seq 3 | sed '2a hello'
<br>

## OUTPUT

![o39](/39.png)
<br>

seq 2 | sed '2i hello'
<br>

## OUTPUT

![o40](/40.png)
<br>

seq 10 | sed '2,9c hello'
<br>

## OUTPUT

![o41](/41.png)
<br>

sed -n '2,4{s/^/$/;p}' file23
<br>

## OUTPUT

![o42](/42.png)
<br>

sed -n '2,4{s/$/*/;p}' file23
<br>

## OUTPUT

![o43](/43.png)
<br>

#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | Tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sid |  7000 | Dev
``` 
sort file21
<br>

## OUTPUT

![o44](/44.png)
<br>

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | Tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sid |  7000 | Dev
``` 
uniq file22
<br>

## OUTPUT

![o45](/45.png)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
<br>

## OUTPUT

![o44](/46.png)
<br>

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
<br>

## OUTPUT

![o47](/47.png)
<br>
 
cat urllist.txt | tr -d ' ' | tr -s '.'
<br>

## OUTPUT

![o48](/48.png)
<br>

# Backup commands
tar -cvf backup.tar *
<br>

## OUTPUT

![o49](/49.png)
<br>

```
mkdir backupdir
 
mv backup.tar backupdir
 
tar -cvf backup.tar *

tar -tvf backup.tar
```
<br>

## OUTPUT

![o50](/50.png)

tar -xvf backup.tar
<br>

## OUTPUT

![o51](/51.png)
<br>

```
gzip backup.tar

ls *.gz
```
<br>

## OUTPUT

![o52](/52.png)
 
gunzip backup.tar.gz
<br>

## OUTPUT

![o53](/53.png)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘ >> my-script,sh
echo 'exit 0' >> my-script.sh

chmod 755 my-script.sh
./my-script.sh
```

## OUTPUT

![o54](/54.png)
<br>
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![o55](/55.png)
<br>

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
<br>

## OUTPUT

![o56](/56.png)
<br>
 
ls file1
<br>

## OUTPUT

![o57](/57.png)
<br>

echo $?
<br>

## OUTPUT 

![o58](/58.png)
<br>

./one
bash: ./one: Permission denied
 
echo $?
<br>

## OUTPUT 

![o59](/59.png)
<br>
  
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

![o60](/60.png)
<br>

chmod 755 strcomp.sh
 
./strcomp.sh 
<br>

## OUTPUT

![o61](/61.png)
<br>

# check file ownership
cat > psswdperm.sh 
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
<br>

## OUTPUT

![o62](/62.png)
<br>

# check if with file location
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
<br>

## OUTPUT

![o63](/63.png)
<br>

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

![o64](/64.png)

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

![o65](/65.png)
<br>

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

![o66](/66.png)

# testing compound comparisons
cat > ifcompound.sh 
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

![o67](/67.png)
<br>

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

![o68](/68.png)
 
cat > whiletest
```bash
\#!/bin/bash
\#while command test
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

![o69](/69.png)
<br>
 
cat > untiltest.sh 
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
$ ./untiltest.sh 

## OUTPUT

![o70](/70.png)
<br>
 
cat > forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
 
$ chmod 755 forin1.sh
$ ./forin1.sh 

## OUTPUT

![o71](/71.png)
<br>
 
cat > forin2.sh 
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

![o72](/72.png)
<br>
 
cat > forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh
$ ./forin3.sh 

## OUTPUT

![o73](/73.png)
<br>
 
cat > forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh
$ ./forin1.sh

## OUTPUT

![o74](/74.png)
<br>

cat > forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ ./forinfile.sh
$ cat > cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

![o75](/75.png)
<br>

cat > forctype.sh 
```bash
#!/bin/bash
#testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```

$ chmod 755 forctype.sh
$ ./forctype.sh 

## OUTPUT

![o76](/76.png)
<br>

cat > forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT

![o77](/77.png)
<br>

cat > fornested1.sh 
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

![o78](/78.png)
<br>
 
cat > forbreak.sh 
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

![o79](/79.png)
<br> 
 
cat > forcontinue.sh 
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

![o80](/80.png)
<br>
 
cat > exread.sh 
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

![o81](/81.png)
<br>

cat > exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh 

## OUTPUT

![o82](/82.png)
<br>
 
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

![o83](/83.png)
<br>
 
cat > argshift.sh
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

![o84](/84.png)
<br>
 
cat > argshift1.sh
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

![o85](/85.png)
<br>

cat > argshift.sh
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

![o86](/86.png)
<br> 
 
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
cat > data.dat
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

![o87](/87.png)
<br>
 
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
![o88](/88.png)
<br>

# RESULT:
The Commands are executed successfully.
