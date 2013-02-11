# How to be a Terminal Pro
https://tutsplus.com/course/how-to-be-a-terminal-pro/

## Introduction

### Hello Terminal
* `echo 'hello word!'` - prints `hello world!` to the command line with a line break
* `echo -n 'hello!'` - will supresses the newline, but it looks like my oh-my-zsh installation doesn't make it look quite like bashrc
* The ~ on a Mac is /Users/neilkelty by default
* Press `Ctrl + A` to go to the beginning of a long line
* Press `Ctrl + E` to go to the end of a long line
* Press the up key to go in my history of command
* Tab-completion - when you start typing out the filename, you can hit `tab` and it will either complete the file path or hitting `tab` twice will give you the options if there are multiple
* Type `clear` to clear the terminal screen - you can still scroll up and see everything, just gives you a blank slate
* Type in `man echo` or any other command for the manual/documentation

### Navigating the File System
* `ls Documents` - list out the contents of the Documents Directory
* `ls Documents Music` - list out the contents of the Documents and Music directories (separately, of course)
* `pwd` - print out working directory
* Case-sensitivity will work on Mac, but not on Unix in general - so be careful about this
* You can't leave a space in the file name - so you have two options `ls Some\ Documents` or `ls "Some Directory"`
* `ls -l` - gives me a detailed list
* `ls -a` - gives me all the files in a directory - including hidden files
* `ls -t` - sorts the files by the time they were last modified
* `ls -t -l -a`, `ls -tla`, or `ls -alt` - sort the files by the time they were last modified, gives me a detailed list, and gives me all the files
* `cd Dcouments` - change to the documents folder
* `cd .` - current directory
* `cd ..` - one level up
* You can drag a file from Finder right into the Terminal to specify the absolute path
* `open .` - opens the current directory in the finder
* `open aFile.txt` - will open the default application for that file
* `open -a Pages aFile.txt` - will open that file with a specific application
* `open -R aFile.txt` - opens that file and highlights it in Finder
* `open http://www.google.com` - opens the website in the default browser

### Files, Links, and CRUD
* `touch superimportantfile.txt` - creates file
* `nano superimportantfile.txt` - gives a text editor in the terminal to edit the file
* `mkdir adir` - creates a directory
* `touch adir/anotherfile.txt` - creates another file in that directory
* `cp afile afile.bak` - creates a copy of a file
* `cp -r adir seconddir` - the `-r` is the recursive option and lets you copy the directory and all the files in the directory
* `mv afile adir` - move afile to adir
* `mv afile ~/adir/afile-backup` - moves `afile` to the `adir` directory and renames the file `afile-backup`
* `mv afile secondfile` - renames `afile` to `secondfile`
* `mv file* adir/` - moves all the files starting with `file` to the `adir` directory. You can use this `*` with touch, etc.
* `rm afile` - deletes `afile`
* `rmdir folderr` - removes a folder - but if there's a file in the folder it won't work. You have to do `rm -r folderr` command
* `ln -s afile symlinkforafile` - creates a symboliclink, the `-s` stands for soft link. The symlinkforafile will be the same as afile. But if you move/rename `afile` with a soft link, the symbolic link will be broken. But if you do a hard link `ln afile2 hardlinkforafile2` then the link won't get broken by moving/renaming the file. 