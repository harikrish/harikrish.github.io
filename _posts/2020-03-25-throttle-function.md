---
layout: post
title:  "Throttle function"
date:   2020-03-25 06:35:48 -0700
categories: JavaScript
---

A throttle is a cousin of the debounce, and they both improve the performance of web applications. 

A throttle is best used when you want to handle all intermediate states but at a controlled rate. 

Throttling enforces a maximum number of times a function can be called over time. As in "execute this function at most once every 100 milliseconds."

{% highlight javascript %}
// code from https://css-tricks.com/the-difference-between-throttling-and-debouncing/

$("body").on('scroll', _.throttle(function() {
  // Do expensive things
}, 100));

{% endhighlight %}

References:
- https://levelup.gitconnected.com/throttle-in-javascript-improve-your-applications-performance-984a4e020a3f
- https://css-tricks.com/the-difference-between-throttling-and-debouncing/
- https://highrise.digital/blog/how-to-throttle-javascript-functions/