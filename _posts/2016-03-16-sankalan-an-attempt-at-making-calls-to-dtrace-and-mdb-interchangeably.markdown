---
author: prashant
comments: true
date: 2016-03-16 00:25:39+00:00
layout: post
link: http://prashant.at/blog/?p=34
slug: sankalan-an-attempt-at-making-calls-to-dtrace-and-mdb-interchangeably
title: 'Sankalan : An attempt at making calls to dtrace and mdb interchangeably.'
wordpress_id: 34
---

**Introduction**

The point of this project to allow a set of methods to make dtrace and mdb calls from within a ruby program

**Motivation**

There were cases in our midterm, wherein we had to catch a certain syscall on dtrace, then inspect the code using mdb. 

**Implementation**

I implemented a module called Sankalan, with separate classes for Processes, generic methods and a class for File. 

We make calls to mdb using the shell calls, and similarly calls to dtrace through the shell calls.

**Code :**

I hosted the code at https://github.com/prashantbarca/sankalan

**Future Directions**

- Supporting more methods
- Testing
