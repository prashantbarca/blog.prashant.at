---
author: prashant
comments: true
date: 2016-03-07 21:17:40+00:00
layout: post
link: http://prashant.at/blog/?p=30
slug: installing-ruby-using-rbenv-on-openindiana-illumos-11-hipster
title: Installing Ruby using Rbenv on OpenIndiana Illumos 11 (Hipster)
wordpress_id: 30
categories:
- Ruby
- Tech
---

If you have been trying to uninstall the preinstalled version of ruby, you would have seen that dtrace has a dependency of ruby, and wouldn't let you uninstall ruby.

In order to solve this, I try to install ruby using rbenv, using the usual commands.


<blockquote>

>     
>     git clone https://github.com/rbenv/rbenv.git <span class="pl-k">~</span>/.rbenv
>     <span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>export PATH="$HOME/.rbenv/bin:$PATH"<span class="pl-pds">'</span></span> <span class="pl-k">>></span> <span class="pl-k">~</span>/.bashrc
>     source ~/.bashrc
>     <code>git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build</code>
>     rbenv install 2.3.0 (Or the version you want)
>     rbenv rehash
>     <span class="pl-c1">echo</span> <span class="pl-s"><span class="pl-pds">'</span>export PATH="$HOME/.rbenv/versions/2.3.0/bin:$PATH"<span class="pl-pds">'</span></span> <span class="pl-k">>></span> <span class="pl-k">~</span>/.bashrc
> 
> 


> 
> * * *
> 
> 

</blockquote>


Following this, we need to remove the presently version of ruby. I just directly removed it, without thinking about the repercussions.
If you want to do the same, just run the following command. 

    
    
    $ sudo rm -rf /usr/ruby 
    $ rbenv rehash
