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

<img width="363" height="123" alt="image" src="https://github.com/user-attachments/assets/0ab031c0-c5bb-4b31-9d84-cc24025ac41f" />



cat < file2
## OUTPUT

<img width="356" height="136" alt="image" src="https://github.com/user-attachments/assets/944632c6-57aa-4077-9499-cefbe3477fec" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="390" height="59" alt="image" src="https://github.com/user-attachments/assets/570e15cc-8250-464c-b883-ecf246482026" />
 

comm file1 file2
 ## OUTPUT
<img width="410" height="181" alt="image" src="https://github.com/user-attachments/assets/eb426057-d6cb-43ae-b52b-12d432741aa1" />


 
diff file1 file2
## OUTPUT

<img width="421" height="221" alt="image" src="https://github.com/user-attachments/assets/9632c668-2cfa-424b-b026-5ad1e6661a39" />


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


<img width="421" height="70" alt="image" src="https://github.com/user-attachments/assets/09078119-418f-44dc-bdc1-87621d7cee22" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="442" height="92" alt="image" src="https://github.com/user-attachments/assets/0fcb1505-6e24-41fd-85d0-81b7ab116b41" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="92" alt="image" src="https://github.com/user-attachments/assets/00a4426a-21d8-4c93-9ba7-eff82ddc6f33" />




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

<img width="402" height="56" alt="image" src="https://github.com/user-attachments/assets/6e4603e5-d5f6-4aad-8d00-bde0c44c8fb8" />



grep hello newfile 
## OUTPUT


<img width="456" height="48" alt="image" src="https://github.com/user-attachments/assets/b70f9f6e-8a18-426c-bfc1-37ac58217af4" />



grep -v hello newfile 
## OUTPUT

<img width="456" height="48" alt="image" src="https://github.com/user-attachments/assets/febe96da-3d08-47e0-bc7c-8f82990ee9d1" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="516" height="70" alt="image" src="https://github.com/user-attachments/assets/0b5707a2-8802-488a-a5a7-d7e29eea6b29" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="552" height="50" alt="image" src="https://github.com/user-attachments/assets/5d33f8d2-155d-4f9b-b364-63ed4cca9ee6" />



grep -R ubuntu /etc
## OUTPUT

<img width="1854" height="1048" alt="image" src="https://github.com/user-attachments/assets/b09ce733-44b0-44f3-bc55-5d50551083c8" />


grep -w -n world newfile   
## OUTPUT
<img width="468" height="70" alt="image" src="https://github.com/user-attachments/assets/6d685278-ee35-4660-bb74-728115b9e6d9" />


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


<img width="520" height="70" alt="image" src="https://github.com/user-attachments/assets/449acded-ca30-431b-a20a-ffd5090e4053" />

egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="520" height="70" alt="image" src="https://github.com/user-attachments/assets/71a2c33c-e1dc-4b68-9fd0-06b75b5fec39" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="553" height="72" alt="image" src="https://github.com/user-attachments/assets/c9103974-2729-429b-b7f8-0aebdc1e5c62" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="553" height="51" alt="image" src="https://github.com/user-attachments/assets/299c51ab-01a0-4edc-b41d-4ef712fee9fb" />


egrep '(world$)' newfile 
## OUTPUT

<img width="553" height="51" alt="image" src="https://github.com/user-attachments/assets/215db4a1-b69d-4a1b-8324-85badcc9b46b" />



egrep '(World$)' newfile 
## OUTPUT

<img width="546" height="76" alt="image" src="https://github.com/user-attachments/assets/57f7321c-5138-49a7-bde2-67a54b81f8e6" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="538" height="91" alt="image" src="https://github.com/user-attachments/assets/57962e7e-8e5f-4ef3-a0f0-c1e704cfe9c2" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="538" height="50" alt="image" src="https://github.com/user-attachments/assets/dcfae080-86cd-40bd-804b-95c4e76471a7" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="538" height="50" alt="image" src="https://github.com/user-attachments/assets/744eddc4-45ad-402d-860f-86293da02a07" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="538" height="50" alt="image" src="https://github.com/user-attachments/assets/43e1f2e3-62f2-4119-8795-b3eb9c66c65a" />



egrep l{2} newfile
## OUTPUT

<img width="536" height="72" alt="image" src="https://github.com/user-attachments/assets/be3dfaf5-446b-4486-900a-179415079fe8" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="536" height="95" alt="image" src="https://github.com/user-attachments/assets/d42ad9fb-b03d-4654-b115-c1dcc87c80ee" />

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
<img width="450" height="52" alt="image" src="https://github.com/user-attachments/assets/e705e4d2-f959-43c0-a5e8-b729ec65dcf7" />



sed -n -e '$p' file23
## OUTPUT



















sed  -e 's/Ram/Sita/' file23
## OUTPUT








![Uploading image.png…]()



sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-40-18.png>)

sed -n -e '1,5p' file23
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-41-20.png>)

sed -n -e '2,/Joe/p' file23
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-42-25.png>)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-43-17.png>)

seq 10 
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-43-39.png>)

seq 10 | sed -n '4,6p'
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-44-14.png>)

seq 10 | sed -n '2,~4p'
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-44-59.png>)

seq 3 | sed '2a hello'
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-46-05.png>)

seq 2 | sed '2i hello'
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-46-53.png>)

seq 10 | sed '2,9c hello'
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-47-54.png>)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-49-44.png>)


sed -n '2,4{s/$/*/;p}' file23

![alt text](<Screenshot from 2026-02-04 21-51-56.png>)

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

![alt text](<Screenshot from 2026-02-04 21-53-09.png>)

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

![alt text](<Screenshot from 2026-02-04 21-54-03.png>)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-56-09.png>)

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

![alt text](<Screenshot from 2026-02-04 21-58-29.png>)
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![alt text](<Screenshot from 2026-02-04 21-59-33.png>)

#Backup commands
tar -cvf backup.tar *
## OUTPUT

![alt text](<Screenshot from 2026-02-04 22-00-37.png>)

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![alt text](<Screenshot from 2026-02-04 22-02-38.png>)

tar -xvf backup.tar
## OUTPUT

![alt text](<Screenshot from 2026-02-04 22-04-06.png>)

gzip backup.tar

ls .gz
## OUTPUT
 
![alt text](<Screenshot from 2026-02-04 22-05-19.png>)

gunzip backup.tar.gz
## OUTPUT

![alt text](<Screenshot from 2026-02-04 22-06-09.png>)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![alt text](<Screenshot from 2026-02-04 22-17-21.png>)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![alt text](<Screenshot from 2026-02-04 22-19-33.png>)

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

![alt text](<Screenshot from 2026-02-04 22-51-25.png>)
 
ls file1
## OUTPUT

![alt text](<Screenshot from 2026-02-04 22-52-52.png>)

echo $?
## OUTPUT 

![alt text](<Screenshot from 2026-02-04 22-53-12.png>)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
![alt text](<Screenshot from 2026-02-04 22-59-17.png>)

abcd
 
echo $?
 ## OUTPUT

![alt text](<Screenshot from 2026-02-04 23-00-05.png>)
 
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

![alt text](<Screenshot from 2026-02-04 23-03-39.png>)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![alt text](<Screenshot from 2026-02-04 23-07-00.png>)

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

![alt text](<Screenshot from 2026-02-04 23-12-36.png>)

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

![alt text](<Screenshot from 2026-02-04 23-16-47.png>)

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

![alt text](<Screenshot from 2026-02-04 23-16-47-1.png>)

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

![alt text](<Screenshot from 2026-02-04 23-21-52.png>)

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

![alt text](<Screenshot from 2026-02-04 23-27-14.png>)

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

![alt text](<Screenshot from 2026-02-04 23-33-01.png>)

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

## output

![alt text](<Screenshot from 2026-02-04 23-37-27.png>)
 
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

## output

![alt text](<Screenshot from 2026-02-04 23-44-19.png>)
 
 
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
 
 ![alt text](<Screenshot from 2026-02-04 23-47-24.png>)
 
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
 
 ![alt text](<Screenshot from 2026-02-04 23-56-33.png>)
 
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
 
![alt text](<Screenshot from 2026-02-04 23-59-11.png>)

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
 
![alt text](<Screenshot from 2026-02-05 00-02-14.png>)

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

![alt text](<Screenshot from 2026-02-04 23-56-33-1.png>)

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

![alt text](<Screenshot from 2026-02-05 00-07-34.png>)

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

![alt text](<Screenshot from 2026-02-05 00-12-43.png>)

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

![alt text](<Screenshot from 2026-02-05 00-14-55.png>)

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

 ![alt text](<Screenshot from 2026-02-05 00-17-54.png>)

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

![alt text](<Screenshot from 2026-02-05 00-20-55.png>)

 
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
 
![alt text](<Screenshot from 2026-02-05 00-23-50.png>)

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

![alt text](<Screenshot from 2026-02-05 00-26-40.png>)

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

![alt text](<Screenshot from 2026-02-05 00-31-12.png>)

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

![alt text](<Screenshot from 2026-02-05 00-33-24.png>)
 
 ./funcex.sh 1 2

 ![alt text](<Screenshot from 2026-02-05 00-33-51.png>)

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
 
![alt text](<Screenshot from 2026-02-05 00-36-28.png>)

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
 
![alt text](<Screenshot from 2026-02-05 00-39-48.png>)

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
 
 ![alt text](<Screenshot from 2026-02-05 00-39-57.png>)
 
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
 
![alt text](<Screenshot from 2026-02-05 00-43-49.png>)

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

![alt text](<Screenshot from 2026-02-05 00-46-27.png>)

# RESULT:
The Commands are executed successfully.
