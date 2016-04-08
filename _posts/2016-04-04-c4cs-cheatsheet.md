---
layout: post
title:  "C4CS Cheatsheet"
date:   2016-04-04
categories: cheatsheet
---

# EECS398 Computing for Computer Scientists -- final cheatsheet

## Virtual Machine
* Features of Virtual Box guest addition:
	* shared folders
	* drag and drop, shared clipboard
	* enable resolution setting
	* mouse pointer integration
	* time  synchronization,shared clipboard

## Unix/Scripting
* Path is an environment variable that specifying a set of directories where executable programs are located. e.g. ls => /bin/ls
* Special variables	
	* `$?`: return value of the most recent command (0 if succeed)
	* `$_`: most recent parameter
	* `$1, $2, $3`: positional parameters
	* `$@`: array of all positional parameters {$1, $2, $3 ...}
	* `$#`: number of propositional parameters

* `set`: prints current environment
* `env`: prints current environment variables "exported"

## Editors
* Vim and Emacs

|   |vim|emacs|
|:---|:---:|:---:|
|save|:w|C-x C-s|
|quit without saving|:q!|C-x C-c n yes|
|save and quit|:wq|C-x C-s C-x C-c|
|search "TODO"|/TODO|C-s TODO|
|find the next "TODO"|n|C-s|

* sed
	* e.g. `sed s/one/zero/ input.txt` replace the first one in the line with zero
	* e.g. `sed s/one/zero/i input.txt` `i` means ignore case
	* e.g. `sed s/one/zero/g input.txt` `g` means global
	* e.g. `sed -i s/one/zero/g input.txt` `-i` means in place

## Git
* `git init`
* `git status`
* `git add`: working directory => staging area (index)
* `git commit`: staging area => repository (object database)
* `git push`
* `git pull`
* workign directory, staging area

## Regrex and grep
* `^`: beginning of a strng
* `$`: end of a string
* `.`: any character

* `grep -c [regex] [dir]`: `-c` means count
* `grep -v [regex] [dir]`: `-v` means invert match
* `grep -f [regex] [file]`: `-f` means file
* `git grep` searches staged files, but not untracked files

## Makefile
* format:

~~~
target: dependency / prerequisite
	command
~~~

* `.PHONY`: targets that are not files
* `make all`: runs the first target that does not start with .
* `-B`: always make
* special variables
	* `$@`: name of the target
	* `$?`: first prerequisite (usually the source file)
	* `$^`: all prerequisite

## GDB
* `break`: break point (e.g. `break if x == 0`, `break main.c::20`, `break function`)
* `step`: step into
* `next`: step over
* `finish`: step out of
* `continue`: to next breakpoint or end
* `frame`: where am i
* `set`: e.g. `set x=1`
* `up`: to caller
* `down`: to callee (after `up`)
* `print`: print value of variable


## Profiling
* `grof`: compiling with `-pg` flag and fun that executable generates `gmon.out`
