--- 
layout: post 
title: "GoboLinux with new development release!"
description: ""
category: "Archive"
tags: [linux, linux news, gogolinux]
---
{% include JB/setup %}  
GoboLinux just released GoboLinux 014.01 Beta 1!

GoboLinux is a Linux distribution that breaks away from the historical UNIX directory hierarchy.

Basically, this means that there are no directories such as /usr and /etc. The main idea of the alternative hierarchy is to store all files belonging to an application in its own separate subtree; therefore we have directories such as /Programs/GCC/2.95.3/lib. To allow the system to find these files, they are logically grouped in directories such as /System/Links/Executables, which, you guessed it, contains symbolic links to all executable files inside the Programs hierarchy.

To maintain backwards compatibility with traditional Unix/Linux apps, there are symbolic links that mimic the Unix tree, such as "/usr/bin -> /System/Links/Executables", and "/sbin -> /System/Links/Executables" (this example shows that arbitrary differentiations between files of the same category were also removed).

Download it <a href="http://www.gobolinux.org/?page=downloads">here</a>.

Read more about it <a href="http://www.gobolinux.org/">here</a>.
