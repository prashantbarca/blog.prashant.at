---
author: prashant
comments: true
date: 2016-02-19 19:08:17+00:00
layout: post
link: http://prashant.at/blog/?p=26
slug: installing-essentials-for-openindiana
title: Installing essentials for OpenIndiana
wordpress_id: 26
---

We have been using OpenIndiana Illumos for our Advanced OS course. I faced a bit of difficulty installing essentials on it, hence this blog post to keep track of what I did to fix it.



	$ sudo pkg uninstall entire

	$ sudo pkg update -v

	$ pkg set-publisher -O http://pkg.openindiana.org/hipster-2015 --search-first openindiana.org

	$ sudo pkg install build-essential

Helped me, hope it helps someone!
