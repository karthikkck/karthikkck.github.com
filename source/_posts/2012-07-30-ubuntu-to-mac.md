---
layout: post
title: "Ubuntu to MAC"
date: 2012-07-30 18:30
comments: true
categories:
---

I recently moved from "Ubuntu 12" to "iMac" system with lion OS 10.7. It is really a motivating factor to work on a iMac system.

I am summarizing few issues faced when I tried to move one of the php projects from ubuntu to iMac.

### Initial setup of MAC (for a web developer)

1. Install XCODE
2. Install command line tool
3. Install python, rvm, ruby (whatever version you need)
4. Install brew (apt-get install in ubuntu -> brew install in mac)
5. I love this combo - mvim, nerdtree, command-t, Ack

### LAMP to MAMP

I faced following issues in moving from LAMP to MAMP:

1. MAMP supports php 5.4.3 and we need to buy MAMP PRO if you need php 5.3
2. So I used XAMPP as an alternative and things worked perfect

### MAC file name case-sensitivity

I prefer to explain this issue with an example:

    loader::model("user.php");

    loader::model("User.php");

on my ubuntu system the above two lines are considered as a single line file load, i.e "user.php" is considered as same as "User.php".

But this does not happen on mac and I had to rename all "User.php" usage in loading files to "user.php"

## Conclusion:

> whatever it is I just love working on a MAC, specially with a iMAC and not with MAC Book Pro

