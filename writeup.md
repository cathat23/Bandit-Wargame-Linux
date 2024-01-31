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

As Shown : https://imgur.com/undefined

Password for Level 10 = 'G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s'

```
