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
```
