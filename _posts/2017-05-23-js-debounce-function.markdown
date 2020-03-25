---
layout: post
title:  "What is a Debounce function?"
date:   2017-05-23 16:36:00 -0700
categories: JavaScript
---

Debounce function returns a function that as long as it
continues to be invoked, will not be triggered. The 
function will be called after it stops being called for 
N milliseconds.

A debounce is a cousin of the throttle, and they both improve 
the performance of web applications.
A debounce is utilized when you only care about the final state. 
For example, waiting until a user stops typing to fetch typeahead search results.

{% highlight javascript %}

// Code from https://davidwalsh.name/javascript-debounce-function

var myEfficientFn = debounce(function() {
	// All the taxing stuff you do
}, 250);

window.addEventListener('resize', myEfficientFn); 

{% endhighlight %}

The myEfficientFn will not be called until 250 milliseconds has 
passed since the last resize event.

References
- https://davidwalsh.name/javascript-debounce-function
- https://levelup.gitconnected.com/debounce-in-javascript-improve-your-applications-performance-5b01855e086