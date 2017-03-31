---
layout: post
title:  "How to configure multi term in Emacs to allow login shell"
date:   2017-03-30 20:20:35 -0700
categories: Emacs
---

To configure multi term in Emacs to allow login shell

{% highlight lisp %}

(setq multi-term-program-switches "--login")

{% endhighlight %}

- Reference

http://stackoverflow.com/questions/19750218/emacs-multi-term-as-a-login-shell
