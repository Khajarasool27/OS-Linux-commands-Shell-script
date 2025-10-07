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

<img width="326" height="181" alt="image" src="https://github.com/user-attachments/assets/dc0c0615-086d-4f63-9d5a-15ce98df7da7" />


cat < file2
## OUTPUT

<img width="297" height="207" alt="image" src="https://github.com/user-attachments/assets/4b4d707e-b1e3-4083-980c-4d5357522c32" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="411" height="78" alt="image" src="https://github.com/user-attachments/assets/0e5ce1b6-ff43-47f7-b8a7-e6b91de01061" />

comm file1 file2
 ## OUTPUT
<img width="443" height="205" alt="image" src="https://github.com/user-attachments/assets/3edebbd9-5671-4b8b-b73d-d4c857cc206e" />

 
diff file1 file2
## OUTPUT
<img width="480" height="276" alt="image" src="https://github.com/user-attachments/assets/2fe9794d-128e-48f0-a115-a10d8da0cd86" />


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
<img width="331" height="125" alt="image" src="https://github.com/user-attachments/assets/0e00b6ae-39a8-4e34-96e6-7e0ee147bed7" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="351" height="153" alt="image" src="https://github.com/user-attachments/assets/93df2890-229f-4368-bec0-60be5ec7673a" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="381" height="155" alt="image" src="https://github.com/user-attachments/assets/9a850935-236e-405d-977f-c205b2f32384" />


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
<img width="360" height="55" alt="image" src="https://github.com/user-attachments/assets/a4a1b8bc-2942-47ef-a1cc-d562586842cf" />

grep hello newfile 
## OUTPUT

<img width="356" height="73" alt="image" src="https://github.com/user-attachments/assets/7cb817c4-4db6-4ed7-8ff7-3f349271bc2a" />


grep -v hello newfile 
## OUTPUT
<img width="408" height="97" alt="image" src="https://github.com/user-attachments/assets/1e3a2bab-c8db-403d-8d74-f9411ca37e3c" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="401" height="75" alt="image" src="https://github.com/user-attachments/assets/2e995a88-12c6-49ce-bf2e-5d8577cbebba" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="472" height="81" alt="image" src="https://github.com/user-attachments/assets/e27238a1-167c-4e43-94d5-2b661fdcde6a" />


grep -R ubuntu /etc
## OUTPUT
<img width="358" height="52" alt="image" src="https://github.com/user-attachments/assets/08c26967-9f49-48e4-8c49-f48f98c94ea9" />

grep -w -n world newfile   
## OUTPUT
<img width="461" height="70" alt="image" src="https://github.com/user-attachments/assets/0d974edc-7ba4-4fa6-9844-9ba4a8c3c040" />

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
<img width="437" height="101" alt="image" src="https://github.com/user-attachments/assets/095b37f4-c500-498c-be3a-c8b025ea90fc" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="407" height="100" alt="image" src="https://github.com/user-attachments/assets/ea01caf7-c9f3-4618-83a4-acfa025fa63c" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="447" height="111" alt="image" src="https://github.com/user-attachments/assets/af745d7e-f699-45a6-a40c-bbd314c07110" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="438" height="70" alt="image" src="https://github.com/user-attachments/assets/c9a3b5dc-44f6-4440-86fb-88bd40d21d9c" />



egrep '(world$)' newfile 
## OUTPUT
<img width="436" height="97" alt="image" src="https://github.com/user-attachments/assets/f0a02f2c-3e47-47a6-97b1-f2db59b32bd3" />

egrep '(World$)' newfile 
## OUTPUT
<img width="461" height="77" alt="image" src="https://github.com/user-attachments/assets/3b832285-a2a8-41f7-9106-6de80bfcef47" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="465" height="126" alt="image" src="https://github.com/user-attachments/assets/d8966bfd-4332-4126-bf73-40b43696e609" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="422" height="82" alt="image" src="https://github.com/user-attachments/assets/e391f598-0c6e-4ebd-a944-37d30c6b61f0" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="731" height="78" alt="image" src="https://github.com/user-attachments/assets/81697835-b1e9-4b77-9273-e08a24dba4e5" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="455" height="81" alt="image" src="https://github.com/user-attachments/assets/4447e419-fe18-480b-889a-0fe593a7149f" />


egrep l{2} newfile
## OUTPUT
<img width="421" height="101" alt="image" src="https://github.com/user-attachments/assets/a7ba4e02-14e5-4c56-a897-6c7737590689" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="420" height="131" alt="image" src="https://github.com/user-attachments/assets/1d7f86ea-dc57-41ba-9779-a44eea6009c0" />


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
<img width="421" height="82" alt="image" src="https://github.com/user-attachments/assets/650be1a9-bf5a-4853-9959-86245c0cf5d0" />

sed -n -e '$p' file23
## OUTPUT


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="387" height="281" alt="image" src="https://github.com/user-attachments/assets/f7c2ba46-3bf8-4400-b601-27ab542eb2a7" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="470" height="281" alt="image" src="https://github.com/user-attachments/assets/e64117d1-0d66-40b6-b32e-2e752087e2f2" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="502" height="273" alt="image" src="https://github.com/user-attachments/assets/bfa96241-b4cb-4547-abca-6be61361b83a" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="410" height="175" alt="image" src="https://github.com/user-attachments/assets/d44c8ef0-5270-49c2-b53b-8ad789a4ecc5" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="472" height="126" alt="image" src="https://github.com/user-attachments/assets/f88922ee-4ff9-4672-a21b-70020cff6731" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="476" height="102" alt="image" src="https://github.com/user-attachments/assets/d18b3589-7775-4594-b251-4f1f715538b7" />



seq 10 
## OUTPUT
<img width="367" height="295" alt="image" src="https://github.com/user-attachments/assets/40ba048e-29c8-4474-bf0e-bfa3c04507ed" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="337" height="127" alt="image" src="https://github.com/user-attachments/assets/d78427c1-9a53-4e3a-9723-054779f82b0d" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="367" height="127" alt="image" src="https://github.com/user-attachments/assets/ce6c81d9-f28d-417e-ac68-c5deea444657" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="427" height="152" alt="image" src="https://github.com/user-attachments/assets/7bdb3c43-e583-487b-8fe5-2323de4ff764" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="382" height="133" alt="image" src="https://github.com/user-attachments/assets/9595b424-5f37-4302-9ea8-490f55ef182b" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="376" height="135" alt="image" src="https://github.com/user-attachments/assets/bd098821-a567-458e-a88a-4d8057d4760b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="435" height="132" alt="image" src="https://github.com/user-attachments/assets/2317b578-4f83-4c83-8a3e-1ee8a5c6777b" />


sed -n '2,4{s/$/*/;p}' file23
<img width="463" height="132" alt="image" src="https://github.com/user-attachments/assets/3bc87eac-6ef0-45e3-8671-da31aefbda3a" />


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
<img width="451" height="181" alt="image" src="https://github.com/user-attachments/assets/0aa9e305-d5ad-4542-a1dd-f51d9488a8b9" />


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
<img width="485" height="170" alt="image" src="https://github.com/user-attachments/assets/cf8d1cc3-ba91-49ac-a295-c8fe7756c11b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="538" height="281" alt="image" src="https://github.com/user-attachments/assets/a2c980ee-b0b7-4971-bb3d-8e11a19e5427" />

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
<img width="418" height="132" alt="image" src="https://github.com/user-attachments/assets/96451eca-4834-4aa8-8560-4d459fb51fa5" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="475" height="137" alt="image" src="https://github.com/user-attachments/assets/f30c5e21-376a-45a2-83be-e13f5d595295" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="462" height="672" alt="image" src="https://github.com/user-attachments/assets/a336b615-d2d9-450a-bf34-dec44749d23f" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1173" height="680" alt="image" src="https://github.com/user-attachments/assets/3831a57a-682c-4843-80f3-270b4789bed6" />


tar -xvf backup.tar
## OUTPUT
<img width="711" height="676" alt="image" src="https://github.com/user-attachments/assets/0f418e2c-916b-43b3-ae5f-28c4a55b5259" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="513" height="106" alt="image" src="https://github.com/user-attachments/assets/716569cf-e39e-4923-8a99-f4d71eca7ab1" />

gunzip backup.tar.gz
## OUTPUT
<img width="532" height="52" alt="image" src="https://github.com/user-attachments/assets/7de590a0-ddde-419a-a7db-d36b0834c064" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="596" height="81" alt="image" src="https://github.com/user-attachments/assets/df816f5a-6bdc-4c8e-ba14-8f80ab54d40e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="447" height="125" alt="image" src="https://github.com/user-attachments/assets/d508d0fd-a605-4f35-8620-f453ccd17e54" />


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
<img width="373" height="51" alt="image" src="https://github.com/user-attachments/assets/86429054-e564-4681-95a8-dc0f6af1811c" />

 
ls file1
## OUTPUT
<img width="405" height="80" alt="image" src="https://github.com/user-attachments/assets/a888a553-6aad-41c1-9fe3-20d8309a13f0" />

echo $?
## OUTPUT 

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="416" height="77" alt="image" src="https://github.com/user-attachments/assets/1abd1485-b0e5-449b-883f-774dd0a96412" />

abcd
 
echo $?
 ## OUTPUT
<img width="483" height="80" alt="image" src="https://github.com/user-attachments/assets/6f8a1c83-b8fb-4739-8849-02084f2ff166" />


 
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

<img width="578" height="47" alt="image" src="https://github.com/user-attachments/assets/2c4d1d77-2be3-43a1-b78f-466a8026602c" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="450" height="52" alt="image" src="https://github.com/user-attachments/assets/f8a960bc-f8a4-4f2b-b215-c19fda1bde9d" />


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
<img width="438" height="53" alt="image" src="https://github.com/user-attachments/assets/ad4c577f-95a1-4f9a-b526-e479777cb6a2" />

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

<img width="577" height="76" alt="image" src="https://github.com/user-attachments/assets/98c03afa-d6f6-457f-8f60-775026127fed" />


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
<img width="428" height="101" alt="image" src="https://github.com/user-attachments/assets/15060083-06bf-409b-bf97-4de727924c12" />

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
<img width="352" height="52" alt="image" src="https://github.com/user-attachments/assets/89cd84ee-e7df-48c4-861c-f5f576ceb5ca" />

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
<img width="425" height="53" alt="image" src="https://github.com/user-attachments/assets/a87f56cf-f1bc-4ed2-a412-be3896d487ae" />


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
