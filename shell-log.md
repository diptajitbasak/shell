# Shell Log

In **practice/**

Created Directory **shell-playground/**

`$ mkdir shell-playground`

- mkdir => Make Directory

Entering Directory **shell-playground/**

`$ cd shell-playground`

- cd => Change Directory

Get Present Working Directory

`$ pwd`

- pwd => Present Working directory

Tag the result as *%1*

This gives us exact location of the directory we are in.

Lets go to root, **/** => Root Directory

`$ cd /`

This directory contains everything in the OS.

Get Present Working Directory

`$ pwd`

Lets see whats in this directory

`$ ls`

- ls => List

Lets move around, entering **bin**

`$ cd bin`

list again

`$ ls`

Lots oof files, lets go back

`cd ..`

- .. => Parent Directory
- . => Current Directory
- ~ => Home Directory

Lets go home

`$ cd ~`

get Location

`$ pwd`

Tag this as *%2*

**/home/hindpos** => **root** then **home** directory then **hindpos** directory

Lets go back to playground, use tag *%1*

`$ cd %1`

List contains

`$ ls`

It should be empty

Lets creates 3 more directories

`$ mkdir games movies songs`

list contains

`$ ls`

Now you see 3 directories

Now lets create another directory in **games**, **strategy**

`$ mkdir games/strategy`

Let list contain of **games**

`$ ls games`

Now lets creates **fiction** within **books**

```
$ mkdir books
$ mkdir books/fiction
```

Possible Wrong Answer

`$ mkdir books/fiction`

This gives an error

`mkdir: cannot create directory 'books/fiction': No such file or directory`

Shortcut

`$ mkdir -p books/fiction`

Lets Remove **movies**

`$ rmdir movies`

- rmdir => Remove Directory

Check by `ls` to see its removed

Lets remove **books** directories

```
$ rmdir books/fiction
$ rmdir books
```

Possible Wrong Solution

`$ rmdir books`

This gives a error

`rmdir: failed to remove 'books': Directory not empty`

Shortcut

`$ rmdir -p books/fiction`

Lets creates some files **temp**, **hello**, **scripts**, **log**.

`$ touch temp hello scripts log`

**Directories is a special type of file. It conatains more file.**

Lets see which are directories and which are normal files

`$ ls -l`

- Minus ( - ) => Optains
- ls -l => Long List

Output

```
total 8
drwxrwxr-x 3 hindpos hindpos 4096 Jul 20 13:21 games
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 hello
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 log
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 scripts
drwxrwxr-x 2 hindpos hindpos 4096 Jul 20 13:19 songs
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 temp
```

See the first column, one starting with **d** is a directory, rest are files.

You can also see the time and date when the files are created.

More Options

`$ ls -lt`

- ls-lt => Long list sorted by time

Output

```
total 8
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 hello
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 log
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 scripts
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 temp
drwxrwxr-x 3 hindpos hindpos 4096 Jul 20 13:21 games
drwxrwxr-x 2 hindpos hindpos 4096 Jul 20 13:19 songs
```

More Options

`$ ls -lrt`

- ls-lt => Long list sorted by time reversed

Output

```
total 8
drwxrwxr-x 2 hindpos hindpos 4096 Jul 20 13:19 songs
drwxrwxr-x 3 hindpos hindpos 4096 Jul 20 13:21 games
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 temp
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 scripts
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 log
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 hello
```

Lets creates some hidden files

**files starting with . are hidden**

`$ touch .mongo`

List to see that its not visible

`$ ls -a`

- ls -a => List all files (hidden too)

Output

```
.  ..  games  hello  log  .mongo  scripts  songs  temp
```

We can create hidden directories too

`$ mkdir .ucantseeme`

lets list them all!

`$ ls -al`

Output

```
total 16
drwxrwxr-x 4 hindpos hindpos 4096 Jul 20 14:38 .
drwxrwxr-x 3 hindpos hindpos 4096 Jul 20 12:48 ..
drwxrwxr-x 3 hindpos hindpos 4096 Jul 20 13:21 games
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 hello
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 log
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:38 .mongo
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 scripts
drwxrwxr-x 2 hindpos hindpos 4096 Jul 20 13:19 songs
-rw-rw-r-- 1 hindpos hindpos    0 Jul 20 14:13 temp
```

Lets take a break!!!
