---
layout: post
title:  "Jekyll server with Ruby 2.7.0 gives 'warning Using the last argument as keyword parameters is deprecated'"
date:   2020-03-20 06:35:48 -0700
categories: ruby jekyll
---

Running Jekyll local server with Ruby 2.7.0 gives warnings as below,

{% highlight bash}

/home/username/.rvm/gems/ruby-2.7.0/gems/jekyll-3.6.3/lib/jekyll/tags/include.rb:193: warning: Using the last argument as keyword parameters is deprecated

{% endhighlight %}

To suppress warnings , see comment here at Github Jekyll issue page,
https://github.com/jekyll/jekyll/issues/7947#issuecomment-587935866

References:
- https://github.com/jekyll/jekyll/issues/7947