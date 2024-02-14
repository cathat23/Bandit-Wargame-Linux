# Bandit Levels 0 - 18
## Level 0

```

First it is expected of us to log into a game by connecting using the username bandit0
We do this by using the command ssh for secure shell
We use the command as such - ssh username@hostname -p portnumber

The username we are supposed to enter is bandit0
hostname is bandit.labs.overthewire.org 
and port number is 2220

making the command - 
'ssh bandit0@bandit.labs.overthewire.org -p 2220'

upon entering this command we get greeted by: 

https://imgur.com/CYpQN6Q

We are promted to enter the password which was given to us as bandit0 and we are greeted with: 

https://i.imgur.com/nicVynq.png

We are now logged into the ctf game bandit woohoo

Now we do the command 'ls' to see files in the directory which is only readme. upon using the 'cat' command as cat readme we can now see the contents of the file and even the password to the next game as shown. We then exit the level which disconnects us from the host using the 'exit' command:

https://i.imgur.com/6TehvOD.png

Password for Level 1 = NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

```

## Level 1

```

Now we login to the 1st level using the command: 'ssh bandit1@bandit.labs.overthewire.org -p 2220' The Password: 'NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL'

Upon entering we use the command 'ls' only to see a filename that is only " - " when trying to use 'cat -' the file does not open and causes a complete unresponsive terminal as it is a special character file. Hence we must use a special type of notation which is './' which quite literally is a path to the file or execute a command in the current directory we are in.
so we use the command 'cat ./-'
we then recieve the password hence we exit.
as shown : 

https://imgur.com/zYlb2QS

Password for Level 2 = rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

```

## Level 2

```

Now we Login to the Second Level using 'ssh bandit2@bandit.labs.overthewire.org -p 2220' with the password as 'rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi'

Upon entering we use the command 'ls' only to see a file called "spaces in this file name" hence upon trying to use 'cat spaces in this file name' we are treated with alot of error lines saying this file does not exist hence we must do the command like this-
" cat 'spaces in this file name' ". when using '' for the file name it can be accessed as long as its a string filename. we then exit after retrieving the password.

As shown : https://imgur.com/LSFni32


Password for Level 3 = aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

```

## Level 3

```

Now we Login to the Third Level using 'ssh bandit3@bandit.labs.overthewire.org -p 2220' with the password as 'aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG'

Upon entering we again use the 'ls' command only to find a file(?) with coloured letters for text. Upon further inspection on the website quoted " The password for the next level is stored in a hidden file in the inhere directory."
hence we must use the 'cd' command to change the directory
which puts a ~/directoryname$ infront of our terminal username@bandit signifying we are in the directory.
we then do ls to see 0 files showing up hence we use the command 'ls -a' to show all files including the hidden ones.
We then use the 'cat' command to open this hideen file shown to us which then presents us with the password. We then exit.

As shown : https://imgur.com/FJNGs5X

Password for Level 4 = 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

```
## Level 4

```
Now we Login to the Fourth Level using 'ssh bandit4@bandit.labs.overthewire.org -p 2220' with the password as '2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe'

Upon entering we use the 'ls' and see the a directory that we must change to. Hence we use the 'cd' command. again we use the ls command only to find multiple files that begin with - hence we must use the ./ to get a direct path.
We use the 'file ./*' command to see the type of all files. The ./ providing a direct path while '*' lets us look at all the files in the directory. This allows us to lookfor the ASCII File in which the password is set. Once found we then use the 'cat ./filename' to get the ascii key. We then exit.

As shown : https://imgur.com/a/5XjcIrR

Password for Level 5 = 'lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR'


```

## Level 5

```
Now we Login to the fifth Level using 'ssh bandit5@bandit.labs.overthewire.org -p 2220' with the password as 'lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR'

Upon Entering we use the 'ls' command see a directory we must change to. We use the 'cd' command to switch to the inhere directory where we then use the command ls again see around 20 files. on the bandit website we have been given parameter for the so called file - human-readable, 1033 bytes in size, not executable. To find this file we can use the find command where we set the parameters that are true as -readable -size 1033c and the one that is false as ! -executable. we Learn this from going through the 'man find' command page. We are then able to find the path to the file that comes under these conditions. we use the command as 'find -readable -size 1033c ! -executable' and are presented with ./maybehere07/.file2. which is the path of the file fitting the conditions hence we just do 'cat ./maybehere07/.file2'. we then exit.

As Shown : https://imgur.com/a/wWEJ08M 

Password for level 6 = 'P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU'


```

## Level 6 

```
Now we Login to the sixth Level using 'ssh bandit6@bandit.labs.overthewire.org -p 2220' with the password as 'P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU'

on the bandit website it is mentioend the password is stored somewhere on the server and has properties / paramaters such as owned by user bandit7, owned by group bandit6, 33 bytes in size. Upon using 'ls' when entering we find 0 files / directories to go to. Hence we must enter the root directory by typing 'cd /' over here we can use the find command as 'find -user bandit7 -group bandit6 -size 33c' we are hence given a long list of files showing access denied. Look for the file which was accessed properly it will have no access denied which is given as ./var/lib/dpkg/info/bandit7.password. Hence we then use cat command to open this path 'cat ./var/lib/dpkg/info/bandit7.password' obtaining the password. we then exit.

As Shown : https://imgur.com/a/ZebT86P and https://imgur.com/cGERm20

Password for Level 7 = 'z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S'

```
## Level 7 

```
Now We login to the 7th Level using 'ssh bandit7@bandit.labs.overthewire.org -p 2220' with the password as 'z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S'

on the website it is seen that The password for the next level is stored in the file data.txt next to the word millionth. upon using ls we find the data.txt file however using cat prints all the data in the file which is nearly 100 lines. hence we use the grep command as 'grep millionth data.txt' and hence find the line with the password next to it. We then exit.
(( UPON FURTHER SOLVING THE COMMAND CAN BE USED AS 'cat data.txt | grep millionth' what the statement does is take the preceding statement cat data.txt and provide it as input to the second statement grep millionth))

As Shown : https://imgur.com/ensj9hV


Password for Level 8 = 'TESKZC0XvTetK0S9xNwm25STk5iWrBvP'

```

## Level 8

```
Now We login to the 8th Level using 'ssh bandit8@bandit.labs.overthewire.org -p 2220' with the password as 'TESKZC0XvTetK0S9xNwm25STk5iWrBvP'

on the website it is seen that The password for the next level is stored in the file data.txt and is the only line of text that occurs only once. Hence we can use the command 'cat data.txt | sort | uniq -u' uniq -u shows all the unique lines only printed once we can also use uniq -c to find the count of how many times a line is printed. We then exit.

As Shown : https://imgur.com/6fhOvLy

Password for Level 9 = 'EN632PlfYiZbn3PhVK3XOGSlNInNE00t'

```

## Level 9

```
Now We Login to the 9th Level using 'ssh bandit9@bandit.labs.overthewire.org -p 2220' with the password as 'EN632PlfYiZbn3PhVK3XOGSlNInNE00t'

on the website it is seen that The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters. Hence we use the files command where we then use redirection to sort using grep to find the lines with = in it. we use the command 'strings data.txt | grep =' We then exit. 

As Shown : https://imgur.com/a/nmuPBhO

Password for Level 10 = 'G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s'

```

## Level 10

```
Now We Login to the 10th Level using 'ssh bandit10@bandit.labs.overthewire.org -p 2220' with the password as 'G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s'

on the website it is seen that The password for the next level is stored in the file data.txt, which contains base64 encoded data. Upon searching what is base64. Upon using the 'cat' command to look at the data in the file we are unable to see our Ascii code as it ends with two "== symbols", and with a quick search on what base64 is on the web, its a type of encoding process that transforms binary to data into a set of characters. hence upon using the cat command we do see data however its encoded. to figure out how base64 encoding works I then used 'man base64' to then see the command to decode a set of data is 'base64 -d'. So we use the command 'cat data.txt | base64 -d' we are redirecting the opened contents of the data.txt file to the command 'base64 -d' which then decodes it. we then exit.

As Shown : https://imgur.com/kemAkfE and https://imgur.com/PTosclu

Password for Level 11 = '6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM'

```

## Level 11

```

Now We Login to the 11th Level using 'ssh bandit11@bandit.labs.overthewire.org -p 2220' with the password as '6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM'

on the website it has been mentioned that the password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions. We are also linked to a wikipedia article relating to a ROT13 algorithim which is a substititution cypher that replaces a letter with the 13th letter after it in the latin alphabet practically making A(1) -> N(14). After researching on stackoverflow article one can see that we can use the 'tr' command -  https://stackoverflow.com/questions/5442436/using-rot13-and-tr-command-for-having-an-encrypted-email-address. After being unable to find a proper translation for this file I have Searched for this specific command parts listed afterwars 'a-zA-Z: This represents a range of characters from 'a' to 'z' (lowercase) and 'A' to 'Z' (uppercase). It includes all the letters of the English alphabet. n-za-mN-ZA-M: This represents the corresponding range of characters after applying ROT13 to the first range. Now we use the command ' cat data.txt | tr '[a-zA-Z]' '[n-za-mN-ZA-M]' ' I believe the first set of the directed command sets the range for the english charcters used, whereas the second set show the translated setfor the second set by doing l1-l2L1-L2 as such then repeats it for capital letters. We then see the password then exit.
P.S it was much easier to just use a algorithim online to translate this code.


As shown : https://imgur.com/5hvvCOp and https://imgur.com/mFGWNiY

Password for Level 12 = 'JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv'

```

## Level 12

```

Now We Login to the 12th level using 'ssh bandit12@bandit.labs.overthewire.org -p 2220' with the password as 'JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv'

On the website it has been mentioend the password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!). when using the manpage it can be seen that we can make a temporary directory. The name "mkdir" stands for "make directory." hence it makes the directory /tmp and then creates a directory within that directory with the name we have provided. We do this with the command 'mkdir /tmp/hadakoi1234'. After this creating a directory in a directory we use the 'cp data.txt /tmp/hadakoi123' command to  copy the file over to our directory in a directory where we can then work with it. The /tmp/hadakoi1234 is a path to the directory. while doing this we must navigate the directories properly when copying from one to another.

From here we try opening the data.txt file with cat command only to bombarded with a code as hexdump. Upon Looking through wikipedia page provided to us we can  see "Some common names for this program function are hexdump, hd, od, xxd and simply dump or even D." on the page. On the overthewirebandit page we can also see one of the commands given to us to use is 'xxd' hence thats the direction we should move in. Upon searching up man xxd on the web we are directed to this webpage https://linux.die.net/man/1/xxd upon which we see commands listed where one is 'xxd -r' which reverts the hexdump file into binary. We use the command called 'cat data.txt | xxd -r' which opens the text file then proceeds to decrypt. Where we see a large amount of output. Next I copied over this data to a new text file by first creating a text file by using the 'touch filename.txt' command then use a redirection after the last command that printed the command using a redirection operator which is '> filename.txt' Finally our command becomes 'cat data.txt | xxd -r > conversion.txt' which then stores our converted data contents into the file.

Now To Understand the Type of File i am Using i use the file 'command name' which is 'file conversion.txt' we see the output conversion.txt: gzip compressed data, was "data2.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 573.

Upon making previous mistakes one would have to convert the filename to that type of data by changing the identifier to continue working with the file. We do this using the 'mv originalfile convertedfile'. https://isshiki.medium.com/gz-bz2-xz-and-tar-d693e33ddb2a

hence i use the command 'mv conversion.txt conversion.gz' .gz is the identifier for a gzip file and only after adding the identifier for the filename can we acess it that way. Now to unzip this packaged file we must use the gzip command from the https://linux.die.net/man/1/gzip upon looking we see the -d should follow gzip to unzip the command hence use 'gzip -d conversion.gz'

Upon doing 'ls' we now see our conversion file with no identifier hence we now do 'file conversion' to see now its a 'conversion: bzip2 compressed data, block size = 900k' Hence we add the file identifier using 'mv conversion conversion.bz2' Considering the identifier is now different we must use a different unzip file unlike gzip by using bzip2 from https://linux.die.net/man/1/bzip2 upon looking we see the -d hence we use the command 'bzip2 -d conversion.bz2'

Upon doing 'ls' we now see our conversion file has no identifier again!!! so now we do 'file conversion' to now see what kind of file and see 'conversion: gzip compressed data, was "data4.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 20480' hence we again change the identifier to bz and then use 'bzip -d conversion.bz'

Upon doing 'ls' we now see our conversion file has no Identifier again :cricat: hence we now do 'file conversion' to see its type and see 'conversion: POSIX tar archive (GNU)' which is a completely new data type upon searching up posix tar we can open this https://linux.die.net/man/1/tar which shows us a command that can extract all files from a tar file. 'tar -xf archive.tar' However because the file is a tar file and not a compressed file liek bzip2 and gzip we need not change the identifier!! so we use 'tar -xf conversion'

We Now do 'ls' and see a new file called data5.bin. again we wanna figure out what kinda of file it is so we do 'file data5.bin' which is a data5.bin: POSIX tar archive (GNU). hence we again use our above command 'tar -xf data5.bin'

Upon doing 'ls' we now see a new file called data6.bin. Again we wanna figure out what kind of file it is so we do 'file data6.bin' which is a data6.bin: bzip2 compressed data, block size = 900k. Because its a compressed file we now must add the identifier .bz2, 'mv data6.bin data6.bin.bz' . After doing this bzip2 -d data6.bin.bz2

Upon doing 'ls' we now see data6.bin pop up again in our directory.... this is great. Now we wanna again figure out what kind of file it is so we do 'file data6.bin' which is a data6.bin: POSIX tar archive (GNU) hence we can now use our tar command without changing the identifier "yay" 'tar -xf data6.bin'

Upon doing 'ls' again we now see data8.bin .Again, Now we wanna  figure out what kind of file it is so we do 'file data8.bin' which is a data8.bin: gzip compressed data, was "data9.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix, original size modulo 2^32 49. We now change the identifier as its a compressed file 'mv data8.bin data8.bin.gz' then proceed to unzip the compressed file using 'gzip -d data8.bin.gz'

Upon doing 'ls' again we now see data8.bin for a 2nd time....................... Why. Now we again wanna figure out what kind of file it is so we do 'file data8.bin' which is a data8.bin: ASCII text which is supposed to be our password?? yooo so now we use the cat command as 'cat data8.bin' to then see our password in all its glory. We then exit.




As Shown : https://imgur.com/qMc12fN and https://imgur.com/AfyC8Jw and https://imgur.com/PDJLzVE


Password for level 13  : wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

```

## Level 13

```
Now We login to the 13th level using 'ssh bandit13@bandit.labs.overthewire.org -p 2220' with the password as 'wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw'

As mentioned on the website The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Over here it seems as though we need to login from the remote machine  we have already connected to with the username bandit14 on the localhost that is the hostname mentioned. Like we did in level0 we can use the ssh command again with 'ssh bandit14@localhost' and as all the other levels use the port numbers 2220 we will also include that as Port numbers in computer networking represent communication endpoints and its the same for every level hence the command then becomes 'ssh bandit14@local host -p 2220'. Yet now we need a password. We have a private key file stored on the bandit13 server hence after a quick search on man ssh and doing ctrl + f and searching for private SSH Key we see another command such as '-i' that Selects a file from which the identity (private key) for RSA or DSA authentication is read https://linux.die.net/man/1/ssh. Hence our final command becomes 'ssh bandit14@localhost -p 2220 -i sshkey.private'. Over here we can now see by our terminal name that we are logged onto bandit 14 and from the hint given that the file is located in '/etc/bandit_pass/bandit14' we can directly open the file with the password by using the 'cat' command followed by our address. We then get shown the password and then exit.

As Shown : https://imgur.com/s6TM9gg and https://imgur.com/ngMAK00

Password for Level 14 : fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq

```

## Level 14 

```

Now We login to the 13th level using 'ssh bandit13@bandit.labs.overthewire.org -p 2220' with the password as 'wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw' We then continue using the command we used to clear the last level to enter the localhost 'ssh bandit14@localhost -p 2220 -i sshkey.private'

As Mentioned on the website The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost. The currents level password we found was 'fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq' Upon Glancing at the commands required for the this level and the promts it would seem that we are required to login to another remote machine this time only submitting our password to port 30000 on the hostname 'localhost' meaning we cannot use ssh like the last level. below other commands are seen to be promted to which we try doing man telnet to see an option to connect to a host with an optional password as seen https://linux.die.net/man/1/telnet. After askimg chatgpt how the command may be used we can see an option where we can use the command 'telnet hostname portnumber' to directly connect with the host and command line interface allowing for us to submit a password which was 'jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt' We then recieve a success prompt and a new password. We then proceed to exit as tghe connection is closed by a foreign host.

As shown : https://imgur.com/a/ETaezYF

```

## Level 15

```

Now We login to level 15 using 'ssh bandit15@bandit.labs.overthewire.org -p 2220' with the password as 'jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt'.

As mentioned on the website The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption. When Looking at the commands prompted to us below we can see the option openssl. upon opening the man openssl we can see that the openssl command opens the commandline tool for ssl. We are required to connect with a server using ssl encryption with the server name local host and the port 30001.
Upon taking help online from a writeup and the official discord server i was provided with the supposed command of 'openssl s_client -connect localhost:30001' Upon researching one can find the openssl as a open-source library that provides support for SSL/TLS protocols. The s_client signifies OpenSSL tool should act as an SSL/TLS client to commit to using SSL encrytption next we have the hostname + port.
After entering this command we are then promted to recieve a password to recieve our next password which we enter as 'jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt'. After which we recieve a correct promt and recieve the password for the next level. It then stops the ssl connection

As Shown : https://imgur.com/a/8oAIIty

Password for Level 16 - 'JQttfApK4SeyHwDlI9SXGR50qclOAil1'

```

## Level 16

```


Now We login to level 16 using 'ssh bandit16@bandit.labs.overthewire.org -p 2220' with the password as 'JQttfApK4SeyHwDlI9SXGR50qclOAil1'.

As mentioned on the website The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. To which only some of these will speak SSL while the others only take in the input and return it to you.
We look at the promted commands to use and we can see the Nmap command which is a command used for network exploration and security auditing as seen here. https://linux.die.net/man/1/nmap. To scan the specific ports we can use the -p command with the range 31000 - 320000. We also must search for these ports on the localhost hence our final command becomes 'nmap localhost -p 31000-32000'. After which we are returned 5 ports that run the protocol and are currently open.
Now we again need to filter through these hosts to find ones that speak SSl so we use the options -sV as it allows us to understand the service version of the port. We also use the -T4 option in Nmap as sets the timing template for the scan. It determines the speed and aggressiveness of the scan. The -T4 timing template is one of several available options, and it strikes a balance between speed and thoroughness. and instead of doing a range like last time we can list out each individual port. hence our cmmand becomes 'nmap localhost -p 31046,31518,31691,31790,31960 -sV -T4'
Upon the returning we see 2 specific ports have SSL as a service hence we need to try connecting to both these ports using the openssl command that we used in the last level. Upon opening the first port level ssl we are seen that we are just being returned our input as output and if looking at the service specified we can see it says SSL/Echo that signifies it will return whatever input. Hence we connect to the other port whith the specific command 'openssl s_client -connect localhost:31790' To which we can then submit the password for this level which is 'JQttfApK4SeyHwDlI9SXGR50qclOAil1' to which we then recieve a RSA private key  which is

'-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----'

Now Like the 12th level we go the temp directorary by using the 'cd /tmp' and make our own directory using 'mkdir hadakoibald' To which we then enter the directory by using 'cd hadakoibald'.
Over here we can save our rsa key by using the nano command off this 'https://www.geeksforgeeks.org/nano-text-editor-in-linux/' to which we use 'nano key' and paste our rsa key in it to which we then just press Ctrl+o to save. Upon doing ls -al we can see that the private key is visible to all people and that should not be possible as it acts like a public key. Hence we must change the permission of the file upon searching online i found this https://www.youtube.com/watch?v=D3YY1RJKzrA to change the permissions of a 'chmod 600 key' where 6 refers to read and write only and 0 means nothing for groups and 0 for people. Now i need to login to the next level usign this key file to which i was promted by someone on the discord server to learn what the command ssh -i command is which literally allows us to directly submit one of our files as the password when connecting to the next level. hence we use the command 'ssh -i key bandit17@localhost -p 2220' as we hare promted to connect on a localhost to which we are then promplty logged in and hence cleared the leve.

As Shown : https://imgur.com/8Qu9YTm

```

## Level 17 

```

As we are already connected from the last level. We then see on the website to be promted There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new. We are also promted several set of commands and the command that stood out the the most was the difference command. First i use the ls command to see what files are in the directory. After confirming the 2 files present we can then use the diff command to which we are returned 2 lines of passwords depending on which order we used the file names in the diff command 'diff passwords.new passwords.old' we see the password was different in the new file and then the password in the old file. the password we recieve is 'hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg' We then exit level 17 and 18 to then connect to level 18.

As SHown : https://imgur.com/tbTXcMu

Password for next Level : 'hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg'

```
