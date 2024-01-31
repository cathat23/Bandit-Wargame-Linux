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

Now we login to the 1st level using the command:
'ssh bandit1@bandit.labs.overthewire.org -p 2220'
The Password:
' NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL '

Upon entering we use the command 'ls' only to see a filename that is only " - " when trying to use 'cat -' the file does not open and causes a complete unresponsive terminal as it is a special character file. Hence we must use a special type of notation which is './' which quite literally is a path to the file or execute a command in the current directory we are in.
so we use the command 'cat ./-'
we then recieve the password hence we exit.
as shown : 

https://imgur.com/zYlb2QS

Password for Level 2 = rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

```

## Level 2

```

Now we Login to the Second Level using ssh 'bandit2@bandit.labs.overthewire.org -p 2220' with the password as 'rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi'

Upon entering we use the command 'ls' only to see a file called "spaces in this file name" hence upon trying to use 'cat spaces in this file name' we are treated with alot of error lines saying this file does not exist hence we must do the command like this-
" cat 'spaces in this file name' ". when using '' for the file name it can be accessed as long as its a string filename. we then exit after retrieving the password.

As shown : https://imgur.com/LSFni32


Password for Level 3 = aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

```

## Level 3

```

Now we Login to the Second Level using ssh 'bandit3@bandit.labs.overthewire.org -p 2220' with the password as 'aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG'

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
Now we Login to the Second Level using ssh 'bandit4@bandit.labs.overthewire.org -p 2220' with the password as '2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe'

Upon entering we use the 'ls' and see the a directory that we must change to. Hence we use the 'cd' command. again we use the ls command only to find multiple files that begin with - hence we must use the ./ to get a direct path.
We use the 'file ./*' command to see the type of all files. The ./ providing a direct path while '*' lets us look at all the files in the directory. This allows us to lookfor the ASCII File in which the password is set. Once found we then use the 'cat ./filename' to get the ascii key. We then exit.

As shown : https://imgur.com/a/5XjcIrR

Password for Level 5 = 'lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR'


```

## Level 5

```




```






