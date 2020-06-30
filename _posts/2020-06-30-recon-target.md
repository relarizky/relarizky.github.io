---
layout: post
title: ReconTarget
subtitle: Web Based Reconnaisance Tool
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

After installation, you can access this tool in http://127.0.0.1:5000 by typing this following

```
$ python3 run.py
```

![Login Page](/assets/img/post/recontarget-login.png)

Then, you can log in to web application with these 2 default users

1. sayang:sayang123 (administrator)
2. hekmen:hekmen123 (ordinary user)

## Role List

There are differences between __administrator__ and __user__ role.

- __administrator__, this role is able to manage user (add, edit, delete) and update the web app
- __ordinary user__, this role is onyle able to perform recon and edit its own profile

![Administrator Page](/assets/img/post/recontarget-administrator.png)
<p style='align:center'>Administrator</p>

![User Page](/assets/img/post/recontarget-user.png)
<p style='align:center'>User</p>

## Manage user

These are some preview of the page of user manager

![User Manager](/assets/img/post/recontarget-manageuser.png)
<p style='align:center'>Manage User</p>

![Edit Profile](/assets/img/post/recontarget-editprofile.png)
<p style='align:center'>Edit Profile</p>

![Add User](/assets/img/post/recontarget-adduser.png)
<p style='align:center'>Add User</p>

![Edit User](/assets/img/post/recontarget-edituser.png)
<p style='align:center'>Edit User</p>
