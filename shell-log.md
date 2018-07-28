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

Lets Delete a file **log**

`$ rm log`

- rm => Remove (Not For Direcroies)

Lets take an assignment

#### Problem Description

- Create a directory **assignment-1**
- Go inside it
- Create another directory **actors** with directory **heroes** within it
- Create five heroes files within **assignment-1/actors/heroes**
  - **tej**
  - **shahrukh**
  - **vijay**
  - **rao**
  - **mahesh**
- Hide **rao** and **mahesh**
- Create a directory **heroine** in **assignment-1/actors**
- Create two files
  - **samantha**
  - **kajal**
- Now create a hidden directory **underrated**
- Create three files which are hidden
  - **nawaz**
  - **saswato**
  - **boomba**
- Check your work that you have done it correctly
- *Bonus: Use `tree` command*
- delete everything


#### SOLUTION
​
Create block
```
$ mkdir -p assignment-1/actors/heroes
$ cd assignment-1/actors/heroes
$ touch tej shahrukh vijay rao mahesh
$ rm rao mahesh
$ touch .rao .mahesh
$ cd ..
$ mkdir heroines
$ cd heroines
$ touch samantha kajal
$ cd ..
$ mkdir .underrated
$ cd .underrated
$ touch .nawaz .saswato .boomba
$ cd ../..
```
​
Use *tree* command
​
`$ tree`
​
OUTPUT
```
.
└── actors
  ├── heroes
  │   ├── shahrukh
  │   ├── tej
  │   └── vijay
  └── heroine
    ├── kajal
    └── samantha
```
​
`$ tree -a`
​
OUTPUT
```
.
└── actors
  ├── heroes
  │   ├── .mahesh
  │   ├── .rao
  │   ├── shahrukh
  │   ├── tej
  │   └── vijay
  ├── heroine
  │   ├── kajal
  │   └── samantha
  └── .underrated
    ├── .boomba
    ├── .nawaz
    └── .saswato
​
```
​
Starting Delete
​
```
$ cd assignment-1/actors/heroes
$ rm tej shahrukh vijay .rao .mahesh
$ cd ../heroines
$ rm samantha kajal
$ cd ../.underrated
$ rm .nawaz .boomba .saswato
$ cd ..
$ rmdir heroes heroines .underrated
$ cd ..
$ rmdir actors
$ cd ..
$ rmdir assignment-1
```
​
Shortcut
`rm -r assignment-1`
​
- rm -r => recursive delete
​
Turn the create block into a script, save this as **assign1-create.sh**

- Add this into top

`#!/bin/sh`

- Lets run this script

`$ sh assign1-create.sh`

Similarly create a shell script for delete **assign1-delete.sh**

- Lets rename some files **hello** into **renamed-hello**

`$ mv hello renamed-hello`

- mv => Move

`$ ls` to checks its renamed

`$ mv songs scripts games/`

Last argument is the destination



