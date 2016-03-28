---
layout: post
title:  "Makefile Cheatsheet"
date:   2016-03-28 16:01:00 -0400
categories: Makefile
---

#Makefile Cheatsheet

* `$@`: name of the file being generated
* `$?`: first prerequisite (usually the source file)
* `$^`: all prerequisite

e.g.

```
all: main.cpp class.cpp
```

* `$@` evaluates `all`
* `$?` evaluates `main.cpp`
* `$^` evaluates `class.cpp`