---
author: prashant
comments: true
date: 2016-06-04 15:31:56+00:00
layout: post
link: http://prashant.at/blog/?p=37
slug: my-emacs-setup
title: My emacs setup!
wordpress_id: 37
categories:
- Tech
---

Over the past month or so, I have begun being more and more favourable to emacs. I have begun appreciating it more than I ever appreciated vim. The reason for this being learning lisp. More specifically, emacs lisp.

I first installed the MELPA and ELPA package managers, by adding them to the ~/.emacs file.


<blockquote>(require 'package) ;; You might already have this line
(add-to-list 'package-archives
'("melpa" . "https://melpa.org/packages/"))
(when (< emacs-major-version 24)
;; For important compatibility libraries like cl-lib
(add-to-list 'package-archives '("gnu" . "http://elpa.gnu.org/packages/")))
(package-initialize)</blockquote>



I then go on to add files that are important for my speedy dev. 

1. projectile. I have added the keybinding -> C-x p to open a control-p like env in vim. 
It basically allows for a speedy search through the entire current folder structure structure. You can use your arrow keys and press the return key to select the particular file. 



<blockquote>
(global-set-key (kbd "C-x p") 'projectile-find-file)
</blockquote>



2. projectile-rails . This gives me some interesting keybindings. I can press C-c r c/m/v for controllers, models and views. It would search only in the particular folder. I can press C-c r g g for the Gemfile. And there are a lot more bindings to get used to over here - https://github.com/asok/projectile-rails . The console, server and dbconsole commands wouldn't work for me though. I need to look into it more closely in the future. 

3. egg - to make git calls from emacs. The more common ones I use have keybindings. 


<blockquote>
(require 'egg)
(global-set-key (kbd "C-x ga") 'egg-stage-all-files)
(global-set-key (kbd "C-x gs") 'egg-status)
(global-set-key (kbd "C-x gc") 'egg-commit-log-edit)
</blockquote>



4. Yasnippet - this is like snipmate for vim. It comes with a set of pre-installed handy snippets. Like pressing s on ruby mode for #{} etc. 



<blockquote>
(require 'yasnippet)
(yas-global-mode 1)
(electric-pair-mode 1)
</blockquote>



5. Nerdcomment style stuff for emacs is in-built. And hence I make use of -- 


<blockquote>
(global-set-key (kbd "C-x cu") 'uncomment-region)
(global-set-key (kbd "C-x cs") 'comment-region)
(global-set-key (kbd "C-x ci") 'comment-indent)
</blockquote>


 
6. Change-inner -- This is my latest find. I feel its still less stronger than vim, when I can just type `cit` to edit within a tag. This one doesn't have that. Although, it does have support for a lot of other stuff, like double quote, single quotes, brackets, braces, etc. 



<blockquote>
(require 'change-inner)
(global-set-key (kbd "M-i") 'change-inner)
(global-set-key (kbd "M-o") 'change-outer)
</blockquote>



I have a long way to go, but emacs has amazed me in a month more than what vim has in the last 5 years. 

