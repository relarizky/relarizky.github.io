---
layout: post
title: ReconTarget - Web Based Reconnaisance Tool
cover-img: /assets/img/thumbnail/recon-target.png
share-img: https://relarizky.github.io/assets/img/thumbnail/recon-target.png
gh-repo: relarizky/ReconTarget
gh-badges: [fork, follow]
tags: [reconnaisance, information gathering, python]
comments: true
---

***ReconTarget*** is a web based __Reconnaisance__ tool that provide a lot of features for gathering useful information of your target website. This tool is built with __Python__ framework, ***Flask***. This tool is also integrated with database (__MySQL__) for storing your target list and its informations, so you can use it for managing your target list instead of storing it in a raw text file.

## Installation

First of all, you need to create one database by typing this command in your terminal

```
$ sudo mysql -u <ur mysql user> -p -e 'CREATE DATABASE <db you'd like to create>

ex: sudo mysql -u root -p -e 'CREATE DATABASE recon'
```

![Create DB](/assets/img/post/recontarget-createdb.png)

Then, you can type these following for installing the web application

```
$ git clone https://github.com/relarizky/ReconTarget.git
$ cd ReconTarget
$ pip3 install -r requirements.txt
$ chmod +x install.py
$ ./install.py
```

![Installation](/assets/img/post/recontarget-install.png)
