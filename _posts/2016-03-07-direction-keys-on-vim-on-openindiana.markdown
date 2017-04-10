---
author: prashant
comments: true
date: 2016-03-07 20:28:49+00:00
layout: post
link: http://prashant.at/blog/?p=28
slug: direction-keys-on-vim-on-openindiana
title: Direction keys on vim on OpenIndiana
wordpress_id: 28
categories:
- Tech
---

The direction keys on the default vim spit out A B C D on pressing the 4 direction keys while on the 'insert' mode. Although, at first glance, one might say, this is vi, not vim. That's what even I thought.

The fix to this problem was simply adding a ~/.vimrc and adding the line "set nocompatible" to it.


