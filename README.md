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
<img width="420" height="150" alt="Screenshot 2026-07-22 113320" src="https://github.com/user-attachments/assets/4f71bad7-c7f3-4a89-b5e5-6ac47ed55063" />



cat < file2
## OUTPUT
<img width="345" height="178" alt="Screenshot 2026-07-22 113527" src="https://github.com/user-attachments/assets/549defc4-50ce-478d-aec6-7c8429fcc88f" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="361" height="73" alt="Screenshot 2026-07-22 113554" src="https://github.com/user-attachments/assets/6b7b4c90-b8a7-4195-b07a-8d0b6083faa3" />

comm file1 file2
 ## OUTPUT
<img width="422" height="225" alt="Screenshot 2026-07-22 113630" src="https://github.com/user-attachments/assets/0bd9033d-7335-4342-b889-32970dca48b3" />

 
diff file1 file2
## OUTPUT
<img width="450" height="275" alt="Screenshot 2026-07-22 113650" src="https://github.com/user-attachments/assets/a867ea61-1346-4912-a884-5e7c294e89ee" />


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

<img width="373" height="101" alt="image" src="https://github.com/user-attachments/assets/e76050a7-7d2f-4002-b9ed-49e50f8077db" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="352" height="130" alt="image" src="https://github.com/user-attachments/assets/235432e5-0ce6-493d-ab6b-83b7d4fd2e37" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="348" height="131" alt="image" src="https://github.com/user-attachments/assets/05e71e13-485b-4c9c-a302-0d4b9ec0d248" />


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
<img width="327" height="75" alt="image" src="https://github.com/user-attachments/assets/e79e9bde-4d3a-4a93-aad7-04a66801cb8d" />



grep hello newfile 
## OUTPUT

<img width="335" height="68" alt="image" src="https://github.com/user-attachments/assets/e0c8a04a-2338-4ada-8e83-bd67dda8a2a1" />



grep -v hello newfile 
## OUTPUT

<img width="341" height="75" alt="image" src="https://github.com/user-attachments/assets/733a8b9f-6e18-423e-8b60-713a0ddca6ae" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="380" height="106" alt="image" src="https://github.com/user-attachments/assets/3aeafbeb-222a-4b01-987e-14422924cb60" />




cat newfile | grep -i -c "hello"
## OUTPUT



<img width="407" height="80" alt="image" src="https://github.com/user-attachments/assets/3aef834f-88fb-4a7e-a611-dc5190d4ec1c" />




grep -R ubuntu /etc
## OUTPUT


<img width="1463" height="730" alt="image" src="https://github.com/user-attachments/assets/0ad17df4-239e-46bf-9e4c-5be3fcf809c0" />


grep -w -n world newfile   
## OUTPUT


<img width="367" height="105" alt="image" src="https://github.com/user-attachments/assets/3ec200ad-9ded-4b84-948f-5856661d9f1a" />


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

<img width="380" height="96" alt="image" src="https://github.com/user-attachments/assets/c6e8a84a-7b2d-4504-a8c2-b5496dadc8a4" />



egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="372" height="102" alt="image" src="https://github.com/user-attachments/assets/a575ec6b-5287-401d-baa6-a9ad9a76adf8" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="455" height="100" alt="image" src="https://github.com/user-attachments/assets/ea043d54-9ed4-4e92-9fb2-3d95a55d88e4" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="347" height="80" alt="image" src="https://github.com/user-attachments/assets/29fb0d32-2b1d-496c-8555-af998ba2ee84" />


egrep '(world$)' newfile 
## OUTPUT


<img width="337" height="100" alt="image" src="https://github.com/user-attachments/assets/52a48078-561d-4fb5-a5b1-4643d87f6a68" />


egrep '(World$)' newfile 
## OUTPUT


<img width="387" height="73" alt="image" src="https://github.com/user-attachments/assets/b6262f61-ab43-45fa-bf88-803aec8887f9" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="360" height="125" alt="image" src="https://github.com/user-attachments/assets/8ac27552-2d6e-47f6-9c88-345c96911eb4" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="372" height="80" alt="image" src="https://github.com/user-attachments/assets/afd4be23-72e1-4d74-b3d3-8f132023badb" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="353" height="75" alt="image" src="https://github.com/user-attachments/assets/3568e0f2-8fcf-4f87-89e8-5f19fb12b84c" />


egrep 'Linux.*World' newfile 
## OUTPUT


<img width="358" height="75" alt="image" src="https://github.com/user-attachments/assets/35f99a11-3f13-42b7-8823-80a6d326c859" />


egrep l{2} newfile
## OUTPUT


<img width="360" height="102" alt="image" src="https://github.com/user-attachments/assets/93cdbe4e-ac59-4704-b52d-4946f0c09dc1" />


egrep 's{1,2}' newfile
## OUTPUT 


<img width="383" height="122" alt="image" src="https://github.com/user-attachments/assets/73c95fcb-acd4-4a0a-ade8-1ddb9dba5f74" />

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


<img width="372" height="103" alt="image" src="https://github.com/user-attachments/assets/f29a9843-3a56-40a2-8374-4e1cc5b9f554" />


sed -n -e '$p' file23
## OUTPUT


<img width="330" height="72" alt="image" src="https://github.com/user-attachments/assets/4d8877c8-e692-4b8a-bc81-036bc8ceccbc" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="412" height="271" alt="image" src="https://github.com/user-attachments/assets/d7bc3aaa-ca93-43bd-af57-0a6c47b40205" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="410" height="271" alt="image" src="https://github.com/user-attachments/assets/3166b91c-18e0-40bb-8d85-c7fed42c8ed1" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="415" height="278" alt="image" src="https://github.com/user-attachments/assets/caa1dac8-d44a-4830-a8f6-3d635c2ebdb3" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="365" height="198" alt="image" src="https://github.com/user-attachments/assets/fb045d8b-6afa-4e92-95ad-cc4d009cbafc" />


sed -n -e '2,/Joe/p' file23
## OUTPUT



<img width="353" height="150" alt="image" src="https://github.com/user-attachments/assets/065c4902-2cf4-4dcd-a25b-45ec6692c695" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="417" height="132" alt="image" src="https://github.com/user-attachments/assets/9996b57e-e602-494c-8120-47d768ab537d" />


seq 10 
## OUTPUT


<img width="340" height="305" alt="image" src="https://github.com/user-attachments/assets/a91d45aa-16a0-4a7c-8edb-7f507a02e5cb" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="320" height="146" alt="image" src="https://github.com/user-attachments/assets/8b2dd49c-a766-4dfb-ba37-42a284e11019" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="350" height="153" alt="image" src="https://github.com/user-attachments/assets/53ee15e0-cf46-41e3-9021-547137e31b67" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="355" height="175" alt="image" src="https://github.com/user-attachments/assets/81cd09e2-da21-4021-a834-92c11b6e3495" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="330" height="153" alt="image" src="https://github.com/user-attachments/assets/79ce6011-0a11-4974-8db9-7780a5b9932c" />


seq 10 | sed '2,9c hello'
## OUTPUT


<img width="352" height="145" alt="image" src="https://github.com/user-attachments/assets/eaa9e893-e49f-4bc4-8109-e5a30cfea10c" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="410" height="158" alt="image" src="https://github.com/user-attachments/assets/b67018b6-c3b1-42bc-bbb1-ea3624e6229b" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="380" height="150" alt="image" src="https://github.com/user-attachments/assets/17a9a755-563d-498b-b327-48fd44bad57d" />


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

<img width="322" height="167" alt="image" src="https://github.com/user-attachments/assets/54fc6d3f-503d-49b7-ae46-337401ee194e" />

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

<img width="350" height="176" alt="image" src="https://github.com/user-attachments/assets/4ae5fbdf-c543-4acc-bc7b-9ded0a53eecf" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="417" height="252" alt="image" src="https://github.com/user-attachments/assets/df008470-ab14-464c-b375-5b401e1a384d" />

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

<img width="352" height="123" alt="image" src="https://github.com/user-attachments/assets/b2c61cad-9866-406b-99df-5d7e707ab085" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="437" height="120" alt="image" src="https://github.com/user-attachments/assets/33a6dcff-84cd-4c64-9452-e32921d6ca14" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="342" height="427" alt="image" src="https://github.com/user-attachments/assets/8cf48a14-e0af-4a00-8f4e-feaec4ff55dc" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="722" height="647" alt="image" src="https://github.com/user-attachments/assets/6160b747-125f-473b-9c3e-59833daa40d6" />

tar -xvf backup.tar
## OUTPUT
<img width="456" height="472" alt="image" src="https://github.com/user-attachments/assets/37053b14-2351-4398-b241-79a730cd8c96" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="542" height="198" alt="image" src="https://github.com/user-attachments/assets/d9afc967-428a-43da-8e2e-06fc151a6d72" />

gunzip backup.tar.gz
## OUTPUT
<img width="473" height="47" alt="image" src="https://github.com/user-attachments/assets/8ccb216a-5068-49eb-bdd9-80e057de61d8" />

 
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
