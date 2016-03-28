---
layout: post
title:  "How to upgrade node"
date:   2016-03-26 17:56:00 -0400
categories: note
---

#### For Linux

Simply running `sudo apt-get install node` would not upgrade the node.  

First check the version of the node
```
$ node -v
```

To upgrade

```bash
$ curl -sL https://deb.nodesource.com/setup_5.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```